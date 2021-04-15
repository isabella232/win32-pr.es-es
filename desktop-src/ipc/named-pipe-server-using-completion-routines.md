---
description: El ejemplo de código es un servidor de canalización de un solo subproceso que crea una canalización de tipo de mensaje y utiliza operaciones superpuestas.
ms.assetid: 8b73485c-c6f7-44df-9e53-308df2c752e7
title: Servidor de canalización con nombre mediante rutinas de finalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efa3ac238680de5cee701488bc4cd60f6543d991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666246"
---
# <a name="named-pipe-server-using-completion-routines"></a>Servidor de canalización con nombre mediante rutinas de finalización

El ejemplo siguiente es un servidor de canalización de un solo subproceso que crea una canalización de tipo de mensaje y utiliza operaciones superpuestas. Usa las funciones extendidas [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) para realizar operaciones de e/s superpuestas mediante una rutina de finalización que se pone en cola para su ejecución cuando finaliza la operación. El servidor de canalización usa la función [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) , que realiza una operación de espera de alerta que devuelve cuando una rutina de finalización está lista para ejecutarse. La función wait también devuelve cuando se señala un objeto de evento, que en este ejemplo indica que la operación [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) superpuesta ha finalizado (se ha conectado un nuevo cliente). Este servidor de canalización se puede usar con el cliente de canalización descrito en [cliente de canalización con nombre](named-pipe-client.md).

Inicialmente, el servidor de canalización crea una instancia única de la canalización e inicia una operación [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) superpuesta. Cuando un cliente se conecta, el servidor asigna una estructura para proporcionar almacenamiento para esa instancia de canalización y, a continuación, llama a la función [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) para iniciar una secuencia de operaciones de e/s para controlar las comunicaciones con el cliente. Cada operación especifica una rutina de finalización que realiza la siguiente operación en la secuencia. La secuencia finaliza cuando el cliente se desconecta y se cierra la instancia de canalización. Después de iniciar la secuencia de operaciones para el nuevo cliente, el servidor crea otra instancia de canalización y espera a que el siguiente cliente se conecte.

Los parámetros de las funciones [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) especifican una rutina de finalización y un puntero a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . Este puntero se pasa a la rutina de finalización en su parámetro *lpOverLap* . Dado que la estructura **superpuesta** apunta al primer miembro de la estructura asignada para cada instancia de canalización, la rutina de finalización puede utilizar su parámetro *lpOverLap* para tener acceso a la estructura de la instancia de canalización.


```C++
#include <windows.h> 
#include <stdio.h>
#include <tchar.h>
#include <strsafe.h>

#define PIPE_TIMEOUT 5000
#define BUFSIZE 4096
 
typedef struct 
{ 
   OVERLAPPED oOverlap; 
   HANDLE hPipeInst; 
   TCHAR chRequest[BUFSIZE]; 
   DWORD cbRead;
   TCHAR chReply[BUFSIZE]; 
   DWORD cbToWrite; 
} PIPEINST, *LPPIPEINST; 
 
VOID DisconnectAndClose(LPPIPEINST); 
BOOL CreateAndConnectInstance(LPOVERLAPPED); 
BOOL ConnectToNewClient(HANDLE, LPOVERLAPPED); 
VOID GetAnswerToRequest(LPPIPEINST); 

VOID WINAPI CompletedWriteRoutine(DWORD, DWORD, LPOVERLAPPED); 
VOID WINAPI CompletedReadRoutine(DWORD, DWORD, LPOVERLAPPED); 
 
HANDLE hPipe; 
 
int _tmain(VOID) 
{ 
   HANDLE hConnectEvent; 
   OVERLAPPED oConnect; 
   LPPIPEINST lpPipeInst; 
   DWORD dwWait, cbRet; 
   BOOL fSuccess, fPendingIO; 
 
// Create one event object for the connect operation. 
 
   hConnectEvent = CreateEvent( 
      NULL,    // default security attribute
      TRUE,    // manual reset event 
      TRUE,    // initial state = signaled 
      NULL);   // unnamed event object 

   if (hConnectEvent == NULL) 
   {
      printf("CreateEvent failed with %d.\n", GetLastError()); 
      return 0;
   }
 
   oConnect.hEvent = hConnectEvent; 
 
// Call a subroutine to create one instance, and wait for 
// the client to connect. 
 
   fPendingIO = CreateAndConnectInstance(&oConnect); 
 
   while (1) 
   { 
   // Wait for a client to connect, or for a read or write 
   // operation to be completed, which causes a completion 
   // routine to be queued for execution. 
 
      dwWait = WaitForSingleObjectEx( 
         hConnectEvent,  // event object to wait for 
         INFINITE,       // waits indefinitely 
         TRUE);          // alertable wait enabled 
 
      switch (dwWait) 
      { 
      // The wait conditions are satisfied by a completed connect 
      // operation. 
         case 0: 
         // If an operation is pending, get the result of the 
         // connect operation. 
 
         if (fPendingIO) 
         { 
            fSuccess = GetOverlappedResult( 
               hPipe,     // pipe handle 
               &oConnect, // OVERLAPPED structure 
               &cbRet,    // bytes transferred 
               FALSE);    // does not wait 
            if (!fSuccess) 
            {
               printf("ConnectNamedPipe (%d)\n", GetLastError()); 
               return 0;
            }
         } 
 
         // Allocate storage for this instance. 
 
            lpPipeInst = (LPPIPEINST) GlobalAlloc( 
               GPTR, sizeof(PIPEINST)); 
            if (lpPipeInst == NULL) 
            {
               printf("GlobalAlloc failed (%d)\n", GetLastError()); 
               return 0;
            }
 
            lpPipeInst->hPipeInst = hPipe; 
 
         // Start the read operation for this client. 
         // Note that this same routine is later used as a 
         // completion routine after a write operation. 
 
            lpPipeInst->cbToWrite = 0; 
            CompletedWriteRoutine(0, 0, (LPOVERLAPPED) lpPipeInst); 
 
         // Create new pipe instance for the next client. 
 
            fPendingIO = CreateAndConnectInstance( 
               &oConnect); 
            break; 
 
      // The wait is satisfied by a completed read or write 
      // operation. This allows the system to execute the 
      // completion routine. 
 
         case WAIT_IO_COMPLETION: 
            break; 
 
      // An error occurred in the wait function. 
 
         default: 
         {
            printf("WaitForSingleObjectEx (%d)\n", GetLastError()); 
            return 0;
         }
      } 
   } 
   return 0; 
} 
 
// CompletedWriteRoutine(DWORD, DWORD, LPOVERLAPPED) 
// This routine is called as a completion routine after writing to 
// the pipe, or when a new client has connected to a pipe instance.
// It starts another read operation. 
 
VOID WINAPI CompletedWriteRoutine(DWORD dwErr, DWORD cbWritten, 
   LPOVERLAPPED lpOverLap) 
{ 
   LPPIPEINST lpPipeInst; 
   BOOL fRead = FALSE; 
 
// lpOverlap points to storage for this instance. 
 
   lpPipeInst = (LPPIPEINST) lpOverLap; 
 
// The write operation has finished, so read the next request (if 
// there is no error). 
 
   if ((dwErr == 0) && (cbWritten == lpPipeInst->cbToWrite)) 
      fRead = ReadFileEx( 
         lpPipeInst->hPipeInst, 
         lpPipeInst->chRequest, 
         BUFSIZE*sizeof(TCHAR), 
         (LPOVERLAPPED) lpPipeInst, 
         (LPOVERLAPPED_COMPLETION_ROUTINE) CompletedReadRoutine); 
 
// Disconnect if an error occurred. 
 
   if (! fRead) 
      DisconnectAndClose(lpPipeInst); 
} 
 
// CompletedReadRoutine(DWORD, DWORD, LPOVERLAPPED) 
// This routine is called as an I/O completion routine after reading 
// a request from the client. It gets data and writes it to the pipe. 
 
VOID WINAPI CompletedReadRoutine(DWORD dwErr, DWORD cbBytesRead, 
    LPOVERLAPPED lpOverLap) 
{ 
   LPPIPEINST lpPipeInst; 
   BOOL fWrite = FALSE; 
 
// lpOverlap points to storage for this instance. 
 
   lpPipeInst = (LPPIPEINST) lpOverLap; 
 
// The read operation has finished, so write a response (if no 
// error occurred). 
 
   if ((dwErr == 0) && (cbBytesRead != 0)) 
   { 
      GetAnswerToRequest(lpPipeInst); 
 
      fWrite = WriteFileEx( 
         lpPipeInst->hPipeInst, 
         lpPipeInst->chReply, 
         lpPipeInst->cbToWrite, 
         (LPOVERLAPPED) lpPipeInst, 
         (LPOVERLAPPED_COMPLETION_ROUTINE) CompletedWriteRoutine); 
   } 
 
// Disconnect if an error occurred. 
 
   if (! fWrite) 
      DisconnectAndClose(lpPipeInst); 
} 
 
// DisconnectAndClose(LPPIPEINST) 
// This routine is called when an error occurs or the client closes 
// its handle to the pipe. 
 
VOID DisconnectAndClose(LPPIPEINST lpPipeInst) 
{ 
// Disconnect the pipe instance. 
 
   if (! DisconnectNamedPipe(lpPipeInst->hPipeInst) ) 
   {
      printf("DisconnectNamedPipe failed with %d.\n", GetLastError());
   }
 
// Close the handle to the pipe instance. 
 
   CloseHandle(lpPipeInst->hPipeInst); 
 
// Release the storage for the pipe instance. 
 
   if (lpPipeInst != NULL) 
      GlobalFree(lpPipeInst); 
} 
 
// CreateAndConnectInstance(LPOVERLAPPED) 
// This function creates a pipe instance and connects to the client. 
// It returns TRUE if the connect operation is pending, and FALSE if 
// the connection has been completed. 
 
BOOL CreateAndConnectInstance(LPOVERLAPPED lpoOverlap) 
{ 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 
 
   hPipe = CreateNamedPipe( 
      lpszPipename,             // pipe name 
      PIPE_ACCESS_DUPLEX |      // read/write access 
      FILE_FLAG_OVERLAPPED,     // overlapped mode 
      PIPE_TYPE_MESSAGE |       // message-type pipe 
      PIPE_READMODE_MESSAGE |   // message read mode 
      PIPE_WAIT,                // blocking mode 
      PIPE_UNLIMITED_INSTANCES, // unlimited instances 
      BUFSIZE*sizeof(TCHAR),    // output buffer size 
      BUFSIZE*sizeof(TCHAR),    // input buffer size 
      PIPE_TIMEOUT,             // client time-out 
      NULL);                    // default security attributes
   if (hPipe == INVALID_HANDLE_VALUE) 
   {
      printf("CreateNamedPipe failed with %d.\n", GetLastError()); 
      return 0;
   }
 
// Call a subroutine to connect to the new client. 
 
   return ConnectToNewClient(hPipe, lpoOverlap); 
}

BOOL ConnectToNewClient(HANDLE hPipe, LPOVERLAPPED lpo) 
{ 
   BOOL fConnected, fPendingIO = FALSE; 
 
// Start an overlapped connection for this pipe instance. 
   fConnected = ConnectNamedPipe(hPipe, lpo); 
 
// Overlapped ConnectNamedPipe should return zero. 
   if (fConnected) 
   {
      printf("ConnectNamedPipe failed with %d.\n", GetLastError()); 
      return 0;
   }
 
   switch (GetLastError()) 
   { 
   // The overlapped connection in progress. 
      case ERROR_IO_PENDING: 
         fPendingIO = TRUE; 
         break; 
 
   // Client is already connected, so signal an event. 
 
      case ERROR_PIPE_CONNECTED: 
         if (SetEvent(lpo->hEvent)) 
            break; 
 
   // If an error occurs during the connect operation... 
      default: 
      {
         printf("ConnectNamedPipe failed with %d.\n", GetLastError());
         return 0;
      }
   } 
   return fPendingIO; 
}

VOID GetAnswerToRequest(LPPIPEINST pipe)
{
   _tprintf( TEXT("[%d] %s\n"), pipe->hPipeInst, pipe->chRequest);
   StringCchCopy( pipe->chReply, BUFSIZE, TEXT("Default answer from server") );
   pipe->cbToWrite = (lstrlen(pipe->chReply)+1)*sizeof(TCHAR);
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cliente de canalización con nombre](named-pipe-client.md)
</dt> </dl>

 

 
