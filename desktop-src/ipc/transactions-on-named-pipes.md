---
description: Una transacción de canalización con nombre es una comunicación cliente-servidor que combina una operación de escritura y una operación de lectura en una sola operación de red. Las transacciones mejoran el rendimiento de las comunicaciones de red entre un cliente y un servidor remoto.
ms.assetid: aedce207-7dea-4670-b6dd-0c61b3f6f690
title: Transacciones en canalizaciones con nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 524f9ae453eb958efd59d8ef6ee5adfda12dd2701e4c719be51299e2873913dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963905"
---
# <a name="transactions-on-named-pipes"></a>Transacciones en canalizaciones con nombre

Una transacción de canalización con nombre es una comunicación cliente-servidor que combina una operación de escritura y una operación de lectura en una sola operación de red. Una transacción solo se puede usar en una canalización dúplex de tipo mensaje. Las transacciones mejoran el rendimiento de las comunicaciones de red entre un cliente y un servidor remoto. Los procesos pueden usar las [**funciones TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) [**y CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) para realizar transacciones de canalización con nombre.

La [**función TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) la usa normalmente un cliente de canalización para escribir un mensaje de solicitud en el servidor de canalización con nombre y leer el mensaje de respuesta del servidor. El cliente de canalización debe especificar el acceso GENERIC READ GENERIC WRITE cuando abre su identificador de canalización mediante \_ una llamada a la función \| \_ [**CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) A continuación, el cliente de canalización establece el identificador de canalización en modo de lectura de mensajes mediante una llamada a la [**función SetNamedPipeHandleState.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) Si el búfer de lectura especificado en la llamada a **TransactNamedPipe** no es lo suficientemente grande como para contener todo el mensaje escrito por el servidor, la función devuelve cero y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR \_ MORE \_ DATA. El cliente puede leer el resto del mensaje llamando a la función [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)o [**PeekNamedPipe.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe)

Normalmente, los clientes de canalización llaman a [**TransactNamedPipe,**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) pero también lo puede usar un servidor de canalización.

En el ejemplo siguiente se muestra un cliente de canalización [**que usa TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe). Este cliente de canalización se puede usar con cualquiera de los servidores de canalización enumerados en Vea también.


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   HANDLE hPipe; 
   LPTSTR lpszWrite = TEXT("Default message from client"); 
   TCHAR chReadBuf[BUFSIZE]; 
   BOOL fSuccess; 
   DWORD cbRead, dwMode; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1)
   {
      lpszWrite = argv[1]; 
   }
 
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
         printf("Could not open pipe\n"); 
         return 0;
      }
 
      // All pipe instances are busy, so wait for 20 seconds. 
      if (! WaitNamedPipe(lpszPipename, 20000) ) 
      {
         printf("Could not open pipe\n"); 
         return 0;
      }
  } 
 
   // The pipe connected; change to message-read mode. 
   dwMode = PIPE_READMODE_MESSAGE; 
   fSuccess = SetNamedPipeHandleState( 
      hPipe,    // pipe handle 
      &dwMode,  // new pipe mode 
      NULL,     // don't set maximum bytes 
      NULL);    // don't set maximum time 
   if (!fSuccess) 
   {
      printf("SetNamedPipeHandleState failed.\n"); 
      return 0;
   }
 
   // Send a message to the pipe server and read the response. 
   fSuccess = TransactNamedPipe( 
      hPipe,                  // pipe handle 
      lpszWrite,              // message to server
      (lstrlen(lpszWrite)+1)*sizeof(TCHAR), // message length 
      chReadBuf,              // buffer to receive reply
      BUFSIZE*sizeof(TCHAR),  // size of read buffer
      &cbRead,                // bytes read
      NULL);                  // not overlapped 

   if (!fSuccess && (GetLastError() != ERROR_MORE_DATA)) 
   {
      printf("TransactNamedPipe failed.\n"); 
      return 0;
   }
 
   while(1)
   { 
      _tprintf(TEXT("%s\n"), chReadBuf);

      // Break if TransactNamedPipe or ReadFile is successful
      if(fSuccess)
         break;

      // Read from the pipe if there is more data in the message.
      fSuccess = ReadFile( 
         hPipe,      // pipe handle 
         chReadBuf,  // buffer to receive reply 
         BUFSIZE*sizeof(TCHAR),  // size of buffer 
         &cbRead,  // number of bytes read 
         NULL);    // not overlapped 

      // Exit if an error other than ERROR_MORE_DATA occurs.
      if( !fSuccess && (GetLastError() != ERROR_MORE_DATA)) 
         break;
      else _tprintf( TEXT("%s\n"), chReadBuf); 
   }

   _getch(); 

   CloseHandle(hPipe); 
 
   return 0; 
}
```



Un cliente de canalización usa [**CallNamedPipe para**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) combinar las llamadas de función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) (si es necesario), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)y [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) en una sola llamada. Dado que el identificador de canalización se cierra antes de que se devuelva la función, los bytes adicionales del mensaje se pierden si el mensaje es mayor que el tamaño especificado del búfer de lectura. El ejemplo siguiente es el ejemplo anterior reescrito para usar **CallNamedPipe**.


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   LPTSTR lpszWrite = TEXT("Default message from client"); 
   TCHAR chReadBuf[BUFSIZE]; 
   BOOL fSuccess; 
   DWORD cbRead; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1)
   {
      lpszWrite = argv[1]; 
   }
 
   fSuccess = CallNamedPipe( 
      lpszPipename,        // pipe name 
      lpszWrite,           // message to server 
      (lstrlen(lpszWrite)+1)*sizeof(TCHAR), // message length 
      chReadBuf,              // buffer to receive reply 
      BUFSIZE*sizeof(TCHAR),  // size of read buffer 
      &cbRead,                // number of bytes read 
      20000);                 // waits for 20 seconds 
 
   if (fSuccess || GetLastError() == ERROR_MORE_DATA) 
   { 
      _tprintf( TEXT("%s\n"), chReadBuf ); 
    
      // The pipe is closed; no more data can be read. 
 
      if (! fSuccess) 
      {
         printf("\nExtra data in message was lost\n"); 
      }
   }
 
   _getch(); 

   return 0; 
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servidor de canalización multiproceso](multithreaded-pipe-server.md)
</dt> <dt>

[Servidor de canalización con nombre que usa E/S superpuesta](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[Servidor de canalización con nombre que usa rutinas de finalización](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
