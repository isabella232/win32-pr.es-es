---
title: Desarrollo de cliente mediante identificadores de contexto
description: El único uso que tiene un programa cliente para un identificador de contexto es pasarlo al servidor cada vez que el cliente realiza una llamada a procedimiento remoto.
ms.assetid: fcbdfb1e-4f1e-4d22-9a3e-cf5a29d300d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ff599bebdf042bc2021d53538cff1c0203d2de875bdc52c50a72675b73a47f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931846"
---
# <a name="client-development-using-context-handles"></a>Desarrollo de cliente mediante identificadores de contexto

El único uso que tiene un programa cliente para un identificador de contexto es pasarlo al servidor cada vez que el cliente realiza una llamada a procedimiento remoto. La aplicación cliente no necesita tener acceso al contenido del identificador. No debe intentar cambiar los datos del identificador de contexto de ninguna manera. Los procedimientos remotos que invoca el cliente realizan todas las operaciones necesarias en el contexto del servidor.

Antes de solicitar un identificador de contexto a un servidor, los clientes deben establecer un enlace con el servidor. El cliente puede usar un identificador de enlace automático, implícito o explícito. Con un identificador de enlace válido, el cliente puede llamar a un procedimiento remoto en el servidor **\[ \]** que devuelve un identificador de contexto abierto (no **NULL)** o pasa uno a través de un parámetro out en la lista de parámetros del procedimiento remoto.

Los clientes pueden usar identificadores de contexto abiertos de la forma que necesiten. Sin embargo, deben invalidar el identificador cuando ya no lo necesiten. Hay dos maneras de hacerlo:

-   Para invocar un procedimiento remoto ofrecido por el programa de servidor que libera el contexto y cierra el identificador de contexto (lo establece en **NULL).**
-   Cuando no se puede acceder al servidor, llame a [**la función RpcSsDestroyClientContext.**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext)

El segundo enfoque solo limpia el estado del lado cliente y no limpia el estado del lado servidor, por lo que solo se debe usar cuando se sospecha de la partición de red y el cliente y el servidor realizarán una limpieza independiente. El servidor realiza una limpieza independiente a través de la rutina de ejecución; el cliente lo hace mediante la [**función RpcSsDestroyClientContext.**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext)

El fragmento de código siguiente presenta un ejemplo de cómo un cliente podría usar un identificador de contexto. Para ver la definición de la interfaz que usa este ejemplo, vea [Desarrollo de interfaces mediante identificadores de contexto.](interface-development-using-context-handles.md) Para la implementación del servidor, vea [Desarrollo del servidor mediante identificadores de contexto.](server-development-using-context-handles.md)

En este ejemplo, el cliente llama a RemoteOpen para obtener un identificador de contexto que contiene datos válidos. A continuación, el cliente puede usar el identificador de contexto en llamadas a procedimiento remoto. Dado que ya no necesita el identificador de enlace, el cliente puede liberar el identificador explícito que usó para crear el identificador de contexto:


```C++
// cxhndlc.c  (fragment of client side application)
printf("Calling the remote procedure RemoteOpen\n");
if (RemoteOpen(&phContext, pszFileName) < 0) 
{
    printf("Unable to open %s\n", pszFileName);
    Shutdown();
    exit(2);
}
 
// Now the context handle also manages the binding.
// The variable hBindingHandle is a valid binding handle.
status = RpcBindingFree(&hBindingHandle);
printf("RpcBindingFree returned 0x%x\n", status);
if (status) 
    exit(status);
```



La aplicación cliente de este ejemplo usa un procedimiento denominado RemoteRead para leer un archivo de datos en el servidor hasta que encuentra un final de archivo. A continuación, cierra el archivo mediante una llamada a RemoteClose. El identificador de contexto aparece como un parámetro en las funciones RemoteRead y RemoteClose como:


```C++
printf("Calling the remote procedure RemoteRead\n");
do 
{
    cbRead = 1024; // Using a 1K buffer
    RemoteRead(phContext, pbBuf, &cbRead);
    // cbRead contains the number of bytes actually read.
    for (int i = 0; i < cbRead; i++)
        putchar(*(pbBuf+i));
} while(cbRead);
 
printf("Calling the remote procedure RemoteClose\n");
if (RemoteClose(&phContext) < 0 ) 
{
    printf("Close failed on %s\n", pszFileName);
    exit(2);
}
```



 

 




