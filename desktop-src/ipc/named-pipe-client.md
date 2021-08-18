---
description: En el ejemplo de código se muestra un cliente de canalización que abre una canalización con nombre, establece el identificador de canalización en modo de lectura de mensajes, usa la función WriteFile para enviar una solicitud al servidor y usa la función ReadFile para leer la respuesta de los servidores.
ms.assetid: 0779242c-45f4-4cd9-9c9f-36cff54c8dee
title: Cliente de canalización con nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d00a3fec3e3d7df80468822d2e147cbae38f440e39fd55dafc9ed3ea2442cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695178"
---
# <a name="named-pipe-client"></a>Cliente de canalización con nombre

Un cliente de canalización con nombre usa [**la función CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un identificador en una canalización con nombre. Si la canalización existe pero todas sus instancias están ocupadas, **CreateFile** devuelve **INVALID HANDLE \_ \_ VALUE** y la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR \_ PIPE \_ BUSY. Cuando esto sucede, el cliente de canalización con nombre usa la [**función WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) para esperar a que una instancia de la canalización con nombre esté disponible.

Se produce un error en la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) si el acceso especificado no es compatible con el acceso especificado (dúplex, saliente o entrante) cuando el servidor creó la canalización. Para una canalización dúplex, el cliente puede especificar el acceso de lectura, escritura o lectura/escritura; para una canalización de salida (servidor de solo escritura), el cliente debe especificar el acceso de solo lectura; y para una canalización de entrada (servidor de solo lectura), el cliente debe especificar el acceso de solo escritura.

El identificador devuelto por [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) tiene como valor predeterminado el modo de lectura de bytes, el modo de bloqueo y espera, el modo superpuesto deshabilitado y el modo de escritura a través deshabilitado. El cliente de canalización puede usar **CreateFile** para habilitar el modo superpuesto especificando FILE FLAG OVERLAPPED o para habilitar el modo de escritura a través \_ \_ especificando FILE \_ FLAG WRITE \_ \_ THROUGH. El cliente puede usar la función [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) para habilitar el modo de no bloqueo especificando PIPE NOWAIT o para habilitar el modo de lectura de mensajes especificando \_ PIPE \_ READMODE \_ MESSAGE.

En el ejemplo siguiente se muestra un cliente de canalización que abre una canalización con nombre, establece el identificador de canalización en modo de lectura de mensajes, usa la función [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) para enviar una solicitud al servidor y usa la función [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) para leer la respuesta del servidor. Este cliente de canalización se puede usar con cualquiera de los servidores de tipo de mensaje enumerados en la parte inferior de este tema. Sin embargo, con un servidor de tipo byte, se produce un error en este cliente de canalización cuando llama a [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) para cambiar al modo de lectura de mensajes. Dado que el cliente está leyendo desde la canalización en modo de lectura de mensajes, es posible que la operación **ReadFile** devuelva cero después de leer un mensaje parcial. Esto sucede cuando el mensaje es mayor que el búfer de lectura. En esta situación, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR MORE DATA y el cliente puede leer el resto del mensaje mediante llamadas \_ \_ adicionales a **ReadFile**.

Este cliente de canalización se puede usar con cualquiera de los servidores de canalización enumerados en Vea también.


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   HANDLE hPipe; 
   LPTSTR lpvMessage=TEXT("Default message from client."); 
   TCHAR  chBuf[BUFSIZE]; 
   BOOL   fSuccess = FALSE; 
   DWORD  cbRead, cbToWrite, cbWritten, dwMode; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1 )
      lpvMessage = argv[1];
 
// Try to open a named pipe; wait for it, if necessary. 
 
   while (1) 
   { 
      hPipe = CreateFile( 
         lpszPipename,   // pipe name 
         GENERIC_READ |  // read and write access 
         GENERIC_WRITE, 
         0,              // no sharing 
         NULL,           // default security attributes
         OPEN_EXISTING,  // opens existing pipe 
         0,              // default attributes 
         NULL);          // no template file 
 
   // Break if the pipe handle is valid. 
 
      if (hPipe != INVALID_HANDLE_VALUE) 
         break; 
 
      // Exit if an error other than ERROR_PIPE_BUSY occurs. 
 
      if (GetLastError() != ERROR_PIPE_BUSY) 
      {
         _tprintf( TEXT("Could not open pipe. GLE=%d\n"), GetLastError() ); 
         return -1;
      }
 
      // All pipe instances are busy, so wait for 20 seconds. 
 
      if ( ! WaitNamedPipe(lpszPipename, 20000)) 
      { 
         printf("Could not open pipe: 20 second wait timed out."); 
         return -1;
      } 
   } 
 
// The pipe connected; change to message-read mode. 
 
   dwMode = PIPE_READMODE_MESSAGE; 
   fSuccess = SetNamedPipeHandleState( 
      hPipe,    // pipe handle 
      &dwMode,  // new pipe mode 
      NULL,     // don't set maximum bytes 
      NULL);    // don't set maximum time 
   if ( ! fSuccess) 
   {
      _tprintf( TEXT("SetNamedPipeHandleState failed. GLE=%d\n"), GetLastError() ); 
      return -1;
   }
 
// Send a message to the pipe server. 
 
   cbToWrite = (lstrlen(lpvMessage)+1)*sizeof(TCHAR);
   _tprintf( TEXT("Sending %d byte message: \"%s\"\n"), cbToWrite, lpvMessage); 

   fSuccess = WriteFile( 
      hPipe,                  // pipe handle 
      lpvMessage,             // message 
      cbToWrite,              // message length 
      &cbWritten,             // bytes written 
      NULL);                  // not overlapped 

   if ( ! fSuccess) 
   {
      _tprintf( TEXT("WriteFile to pipe failed. GLE=%d\n"), GetLastError() ); 
      return -1;
   }

   printf("\nMessage sent to server, receiving reply as follows:\n");
 
   do 
   { 
   // Read from the pipe. 
 
      fSuccess = ReadFile( 
         hPipe,    // pipe handle 
         chBuf,    // buffer to receive reply 
         BUFSIZE*sizeof(TCHAR),  // size of buffer 
         &cbRead,  // number of bytes read 
         NULL);    // not overlapped 
 
      if ( ! fSuccess && GetLastError() != ERROR_MORE_DATA )
         break; 
 
      _tprintf( TEXT("\"%s\"\n"), chBuf ); 
   } while ( ! fSuccess);  // repeat loop if ERROR_MORE_DATA 

   if ( ! fSuccess)
   {
      _tprintf( TEXT("ReadFile from pipe failed. GLE=%d\n"), GetLastError() );
      return -1;
   }

   printf("\n<End of message, press ENTER to terminate connection and exit>");
   _getch();
 
   CloseHandle(hPipe); 
 
   return 0; 
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servidor de canalización multiproceso](multithreaded-pipe-server.md)
</dt> <dt>

[Servidor de canalización con nombre que usa E/S superpuesta](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[Servidor de canalización con nombre mediante rutinas de finalización](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
