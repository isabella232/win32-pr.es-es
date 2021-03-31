---
description: En el ejemplo de código se muestra un cliente de canalización que abre una canalización con nombre, establece el identificador de canalización en modo de lectura de mensaje, utiliza la función WriteFile para enviar una solicitud al servidor y usa la función ReadFile para leer la respuesta de los servidores.
ms.assetid: 0779242c-45f4-4cd9-9c9f-36cff54c8dee
title: Cliente de canalización con nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6318edd7d5b41c701e3112188a896c0529338805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907627"
---
# <a name="named-pipe-client"></a><span data-ttu-id="56e26-103">Cliente de canalización con nombre</span><span class="sxs-lookup"><span data-stu-id="56e26-103">Named Pipe Client</span></span>

<span data-ttu-id="56e26-104">Un cliente de canalización con nombre utiliza la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un identificador a una canalización con nombre.</span><span class="sxs-lookup"><span data-stu-id="56e26-104">A named pipe client uses the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a handle to a named pipe.</span></span> <span data-ttu-id="56e26-105">Si existe la canalización pero todas sus instancias están ocupadas, **CreateFile** devuelve el **\_ \_ valor de identificador no válido** y la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve la canalización de errores \_ \_ ocupada.</span><span class="sxs-lookup"><span data-stu-id="56e26-105">If the pipe exists but all of its instances are busy, **CreateFile** returns **INVALID\_HANDLE\_VALUE** and the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns ERROR\_PIPE\_BUSY.</span></span> <span data-ttu-id="56e26-106">Cuando esto ocurre, el cliente de canalización con nombre usa la función [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) para esperar a que una instancia de la canalización con nombre esté disponible.</span><span class="sxs-lookup"><span data-stu-id="56e26-106">When this happens, the named pipe client uses the [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) function to wait for an instance of the named pipe to become available.</span></span>

<span data-ttu-id="56e26-107">Se produce un error en la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) si el acceso especificado no es compatible con el acceso especificado (dúplex, salida o entrante) cuando el servidor creó la canalización.</span><span class="sxs-lookup"><span data-stu-id="56e26-107">The [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function fails if the access specified is incompatible with the access specified (duplex, outbound, or inbound) when the server created the pipe.</span></span> <span data-ttu-id="56e26-108">En el caso de una canalización dúplex, el cliente puede especificar el acceso de lectura, escritura o lectura y escritura; en el caso de una canalización de salida (servidor de solo escritura), el cliente debe especificar el acceso de solo lectura; y para una canalización de entrada (servidor de solo lectura), el cliente debe especificar el acceso de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="56e26-108">For a duplex pipe, the client can specify read, write, or read/write access; for an outbound pipe (write-only server), the client must specify read-only access; and for an inbound pipe (read-only server), the client must specify write-only access.</span></span>

<span data-ttu-id="56e26-109">El identificador devuelto por [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) tiene como valor predeterminado el modo de lectura de bytes, el modo de espera de bloqueo, el modo superpuesto deshabilitado y el modo de escritura a través deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="56e26-109">The handle returned by [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) defaults to byte-read mode, blocking-wait mode, overlapped mode disabled, and write-through mode disabled.</span></span> <span data-ttu-id="56e26-110">El cliente de canalización puede usar **CreateFile** para habilitar el modo superpuesto especificando la superposición de la marca de archivo \_ \_ o para habilitar el modo de escritura a través especificando la escritura de marca de archivo \_ \_ \_ a través de.</span><span class="sxs-lookup"><span data-stu-id="56e26-110">The pipe client can use **CreateFile** to enable overlapped mode by specifying FILE\_FLAG\_OVERLAPPED or to enable write-through mode by specifying FILE\_FLAG\_WRITE\_THROUGH.</span></span> <span data-ttu-id="56e26-111">El cliente puede usar la función [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) para habilitar el modo de no bloqueo especificando la canalización \_ nowait o para habilitar el modo de lectura de mensajes especificando el mensaje de canalización \_ READMODE \_ .</span><span class="sxs-lookup"><span data-stu-id="56e26-111">The client can use the [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) function to enable nonblocking mode by specifying PIPE\_NOWAIT or to enable message-read mode by specifying PIPE\_READMODE\_MESSAGE.</span></span>

<span data-ttu-id="56e26-112">En el ejemplo siguiente se muestra un cliente de canalización que abre una canalización con nombre, se establece el identificador de canalización en modo de lectura de mensaje, se usa la función [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) para enviar una solicitud al servidor y se usa la función [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) para leer la respuesta del servidor.</span><span class="sxs-lookup"><span data-stu-id="56e26-112">The following example shows a pipe client that opens a named pipe, sets the pipe handle to message-read mode, uses the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function to send a request to the server, and uses the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) function to read the server's reply.</span></span> <span data-ttu-id="56e26-113">Este cliente de canalización se puede usar con cualquiera de los servidores de tipo de mensaje enumerados en la parte inferior de este tema.</span><span class="sxs-lookup"><span data-stu-id="56e26-113">This pipe client can be used with any of the message-type servers listed at the bottom of this topic.</span></span> <span data-ttu-id="56e26-114">Sin embargo, con un servidor de tipo byte, se produce un error en este cliente de canalización cuando llama a [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) para cambiar al modo de lectura de mensajes.</span><span class="sxs-lookup"><span data-stu-id="56e26-114">With a byte-type server, however, this pipe client fails when it calls [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) to change to message-read mode.</span></span> <span data-ttu-id="56e26-115">Dado que el cliente está leyendo de la canalización en modo de lectura de mensajes, es posible que la operación **readfile** devuelva cero después de leer un mensaje parcial.</span><span class="sxs-lookup"><span data-stu-id="56e26-115">Because the client is reading from the pipe in message-read mode, it is possible for the **ReadFile** operation to return zero after reading a partial message.</span></span> <span data-ttu-id="56e26-116">Esto sucede cuando el mensaje es mayor que el búfer de lectura.</span><span class="sxs-lookup"><span data-stu-id="56e26-116">This happens when the message is larger than the read buffer.</span></span> <span data-ttu-id="56e26-117">En esta situación, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve \_ \_ los datos de error y el cliente puede leer el resto del mensaje mediante llamadas adicionales a **readfile**.</span><span class="sxs-lookup"><span data-stu-id="56e26-117">In this situation, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_MORE\_DATA, and the client can read the remainder of the message using additional calls to **ReadFile**.</span></span>

<span data-ttu-id="56e26-118">Este cliente de canalización se puede usar con cualquiera de los servidores de canalización que se enumeran en vea también.</span><span class="sxs-lookup"><span data-stu-id="56e26-118">This pipe client can be used with any of the pipe servers listed under See Also.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="56e26-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56e26-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56e26-120">Servidor de canalización multiproceso</span><span class="sxs-lookup"><span data-stu-id="56e26-120">Multithreaded pipe server</span></span>](multithreaded-pipe-server.md)
</dt> <dt>

[<span data-ttu-id="56e26-121">Servidor de canalización con nombre mediante e/s superpuestas</span><span class="sxs-lookup"><span data-stu-id="56e26-121">Named pipe server using overlapped I/O</span></span>](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[<span data-ttu-id="56e26-122">Servidor de canalización con nombre mediante rutinas de finalización</span><span class="sxs-lookup"><span data-stu-id="56e26-122">Named pipe server using completion routines</span></span>](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
