---
title: La aplicación de servidor
description: El ejemplo siguiente es de la aplicación ' Hola mundo ' en el \\ directorio RPC Hello del kit de desarrollo de software (SDK) de la plataforma.
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e6f13e2c8fecdcff820c62f3076dd2a8edd1a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903500"
---
# <a name="the-server-application"></a>La aplicación de servidor

El ejemplo siguiente es de la aplicación ' Hola mundo ' en el \\ directorio RPC Hello del kit de desarrollo de software (SDK) de la plataforma. El lado servidor de la aplicación distribuida informa al sistema de que sus servicios están disponibles. Después espera las solicitudes del cliente. El compilador MIDL debe usarse con el ejemplo siguiente.

En función del tamaño de la aplicación y las preferencias de codificación, puede elegir implementar procedimientos remotos en uno o varios archivos independientes. En este programa tutorial, el archivo de código fuente Hello. c contiene la rutina del servidor principal. El archivo Hellop. c contiene el procedimiento remoto.

La ventaja de organizar los procedimientos remotos en archivos independientes es que los procedimientos se pueden vincular con un programa independiente para depurar el código antes de que se convierta en una aplicación distribuida. Una vez que los procedimientos funcionan en el programa independiente, puede compilar y vincular los archivos de origen que contienen los procedimientos remotos con la aplicación de servidor. Al igual que con el archivo de origen de la aplicación cliente, el archivo de origen de la aplicación de servidor debe incluir el archivo de encabezado Hello. h.

El servidor llama a las funciones en tiempo de ejecución de RPC [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) y [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) para hacer que la información de enlace esté disponible para el cliente. Este programa de ejemplo pasa el nombre del identificador de interfaz a **RpcServerRegisterIf**. Los demás parámetros se establecen en **null**. A continuación, el servidor llama a la función [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para indicar que está esperando solicitudes de cliente.

La aplicación de servidor también debe incluir las dos funciones de administración de memoria a las que llama el código auxiliar del servidor: la [**\_ \_ asignación de usuarios de MIDL**](the-midl-user-allocate-function.md) y el [**usuario de MIDL \_ \_**](the-midl-user-free-function.md). Estas funciones asignan y liberan memoria en el servidor cuando un procedimiento remoto pasa parámetros al servidor. En este programa de ejemplo, la **\_ \_ asignación de usuarios de MIDL** y el usuario de **MIDL \_ \_ Free** son simplemente contenedores para las funciones de la biblioteca de C [**malloc**](pointers-and-memory-allocation.md) y **Free**. (Tenga en cuenta que, en las declaraciones adelantadas generadas por el compilador MIDL, "MIDL" está en mayúsculas. El archivo de encabezado Rpcndr. h define el usuario de MIDL \_ \_ Free y el \_ usuario \_ de MIDL asigna para que sea gratuito del usuario de MIDL y que el \_ usuario de \_ MIDL \_ \_ asigne, respectivamente).


```C++
/* file: hellos.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h"
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszSecurity         = NULL; 
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned int    cMinCalls = 1;
    unsigned int    fDontWait = FALSE;
 
    status = RpcServerUseProtseqEp(pszProtocolSequence,
                                   RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                                   pszEndpoint,
                                   pszSecurity); 
 
    if (status) exit(status);
 
    status = RpcServerRegisterIf(hello_ServerIfHandle,  
                                 NULL,   
                                 NULL); 
 
    if (status) exit(status);
 
    status = RpcServerListen(cMinCalls,
                             RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                             fDontWait);
 
    if (status) exit(status);
 }

/******************************************************/
/*         MIDL allocate and free                     */
/******************************************************/
 
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t len)
{
    return(malloc(len));
}
 
void __RPC_USER midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 




