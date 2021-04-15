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
# <a name="named-pipe-server-using-completion-routines"></a><span data-ttu-id="360a7-103">Servidor de canalización con nombre mediante rutinas de finalización</span><span class="sxs-lookup"><span data-stu-id="360a7-103">Named Pipe Server Using Completion Routines</span></span>

<span data-ttu-id="360a7-104">El ejemplo siguiente es un servidor de canalización de un solo subproceso que crea una canalización de tipo de mensaje y utiliza operaciones superpuestas.</span><span class="sxs-lookup"><span data-stu-id="360a7-104">The following example is a single-threaded pipe server that creates a message-type pipe and uses overlapped operations.</span></span> <span data-ttu-id="360a7-105">Usa las funciones extendidas [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) para realizar operaciones de e/s superpuestas mediante una rutina de finalización que se pone en cola para su ejecución cuando finaliza la operación.</span><span class="sxs-lookup"><span data-stu-id="360a7-105">It uses the extended functions [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) to perform overlapped I/O using a completion routine, which is queued for execution when the operation is finished.</span></span> <span data-ttu-id="360a7-106">El servidor de canalización usa la función [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) , que realiza una operación de espera de alerta que devuelve cuando una rutina de finalización está lista para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="360a7-106">The pipe server uses the [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) function, which performs an alertable wait operation that returns when a completion routine is ready to execute.</span></span> <span data-ttu-id="360a7-107">La función wait también devuelve cuando se señala un objeto de evento, que en este ejemplo indica que la operación [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) superpuesta ha finalizado (se ha conectado un nuevo cliente).</span><span class="sxs-lookup"><span data-stu-id="360a7-107">The wait function also returns when an event object is signaled, which in this example indicates that the overlapped [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) operation has finished (a new client has connected).</span></span> <span data-ttu-id="360a7-108">Este servidor de canalización se puede usar con el cliente de canalización descrito en [cliente de canalización con nombre](named-pipe-client.md).</span><span class="sxs-lookup"><span data-stu-id="360a7-108">This pipe server can be used with the pipe client described in [Named Pipe Client](named-pipe-client.md).</span></span>

<span data-ttu-id="360a7-109">Inicialmente, el servidor de canalización crea una instancia única de la canalización e inicia una operación [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) superpuesta.</span><span class="sxs-lookup"><span data-stu-id="360a7-109">Initially, the pipe server creates a single instance of the pipe and starts an overlapped [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) operation.</span></span> <span data-ttu-id="360a7-110">Cuando un cliente se conecta, el servidor asigna una estructura para proporcionar almacenamiento para esa instancia de canalización y, a continuación, llama a la función [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) para iniciar una secuencia de operaciones de e/s para controlar las comunicaciones con el cliente.</span><span class="sxs-lookup"><span data-stu-id="360a7-110">When a client connects, the server allocates a structure to provide storage for that pipe instance and then calls the [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) function to start a sequence of I/O operations to handle communications with the client.</span></span> <span data-ttu-id="360a7-111">Cada operación especifica una rutina de finalización que realiza la siguiente operación en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="360a7-111">Each operation specifies a completion routine that performs the next operation in the sequence.</span></span> <span data-ttu-id="360a7-112">La secuencia finaliza cuando el cliente se desconecta y se cierra la instancia de canalización.</span><span class="sxs-lookup"><span data-stu-id="360a7-112">The sequence terminates when the client is disconnected and the pipe instance closed.</span></span> <span data-ttu-id="360a7-113">Después de iniciar la secuencia de operaciones para el nuevo cliente, el servidor crea otra instancia de canalización y espera a que el siguiente cliente se conecte.</span><span class="sxs-lookup"><span data-stu-id="360a7-113">After starting the sequence of operations for the new client, the server creates another pipe instance and waits for the next client to connect.</span></span>

<span data-ttu-id="360a7-114">Los parámetros de las funciones [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) especifican una rutina de finalización y un puntero a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="360a7-114">The parameters of the [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) functions specify a completion routine and a pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="360a7-115">Este puntero se pasa a la rutina de finalización en su parámetro *lpOverLap* .</span><span class="sxs-lookup"><span data-stu-id="360a7-115">This pointer is passed to the completion routine in its *lpOverLap* parameter.</span></span> <span data-ttu-id="360a7-116">Dado que la estructura **superpuesta** apunta al primer miembro de la estructura asignada para cada instancia de canalización, la rutina de finalización puede utilizar su parámetro *lpOverLap* para tener acceso a la estructura de la instancia de canalización.</span><span class="sxs-lookup"><span data-stu-id="360a7-116">Because the **OVERLAPPED** structure points to the first member in the structure allocated for each pipe instance, the completion routine can use its *lpOverLap* parameter to access the structure for the pipe instance.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="360a7-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="360a7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="360a7-118">Cliente de canalización con nombre</span><span class="sxs-lookup"><span data-stu-id="360a7-118">Named Pipe Client</span></span>](named-pipe-client.md)
</dt> </dl>

 

 
