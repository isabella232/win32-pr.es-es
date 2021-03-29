---
title: Desarrollo de interfaces con identificadores de contexto
description: Normalmente, se crea un identificador de contexto especificando el atributo \ context \_ Handle \ en una definición de tipo en el archivo IDL.
ms.assetid: e4caf91f-f92d-4aef-a20f-0a3073230640
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8474d533b27ba1543a9d522dfa4478d306b33cf2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793132"
---
# <a name="interface-development-using-context-handles"></a>Desarrollo de interfaces con identificadores de contexto

Normalmente, se crea un identificador de contexto al especificar el \[ atributo de [**\_ identificador de contexto**](/windows/desktop/Midl/context-handle) \] en una definición de tipo en el archivo IDL. La definición de tipo también especifica implícitamente una rutina de ejecución de contexto que debe proporcionar. Si se interrumpe la comunicación entre el cliente y el servidor, el tiempo de ejecución del servidor invoca esta rutina para realizar cualquier limpieza necesaria. Para obtener más información sobre las rutinas de ejecución de contexto, vea [rutina de ejecución de contexto de servidor](server-context-run-down-routine.md).

Una interfaz que utiliza un identificador de contexto debe tener un identificador de enlace para el enlace inicial, que tiene que tener lugar antes de que el servidor pueda devolver un identificador de contexto. Puede usar un identificador de enlace automático, implícito o explícito para crear el enlace y establecer el contexto.

Un identificador de contexto debe ser del [**tipo \* void**](/windows/desktop/Midl/void) o un tipo que se resuelva como [**void \***](/windows/desktop/Midl/void). El programa de servidor lo convierte al tipo requerido.

> [!Note]  
> Se desaconseja el uso de \[ [**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl) \] para los parámetros de identificador de contexto, excepto para las rutinas que cierran los identificadores de contexto. Si los parámetros de control de contexto marcados \[ [**en**](/windows/desktop/Midl/in), [](/windows/desktop/Midl/out-idl) \] se usan out, no pase un identificador de contexto **nulo** o no inicializado desde el cliente al servidor. En su lugar, se debe pasar un puntero **null** a un identificador de contexto. Tenga en cuenta que los parámetros de identificador de contexto marcados \[ [**en**](/windows/desktop/Midl/in) \] no aceptan punteros **nulos** .

 

En el fragmento siguiente de una definición de interfaz de ejemplo se muestra cómo una aplicación distribuida puede usar un identificador de contexto para que un servidor abra y actualice un archivo de datos para cada cliente.

La interfaz debe contener una llamada a procedimiento remoto para inicializar el identificador y establecerlo en un valor distinto de **null** . En este ejemplo, la función RemoteOpen realiza esta operación. Especifica el identificador de contexto con un \[ [](/windows/desktop/Midl/out-idl) \] atributo direccional out. Como alternativa, podría devolver el identificador de contexto como el valor devuelto del procedimiento. Sin embargo, en este ejemplo, pasaremos el controlador de contexto a través de la lista de parámetros.

En este ejemplo, la información de contexto es un identificador de archivo. Realiza un seguimiento de la ubicación actual en el archivo. La interfaz empaqueta el identificador de archivo como un identificador de contexto y lo pasa como un parámetro a las llamadas a procedimientos remotos. Una estructura contiene el nombre de archivo y el identificador de archivo.

``` syntax
/* file: cxhndl.idl (fragment of interface definition file) */
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE;
typedef [ref] PCONTEXT_HANDLE_TYPE * PPCONTEXT_HANDLE_TYPE;
 
short RemoteOpen([out] PPCONTEXT_HANDLE_TYPE pphContext,
    [in, string] unsigned char * pszFile);
 
void RemoteRead(
    [in] PCONTEXT_HANDLE_TYPE phContext,
    [out, size_is(cbBuf)] unsigned char achBuf[],
    [in, out] short *pcbBuf);
 
short RemoteClose([in, out] PPCONTEXT_HANDLE_TYPE pphContext);
```

La función RemoteOpen crea un identificador de contexto válido y no **nulo** . Pasa el identificador de contexto al cliente. Las llamadas a procedimientos remotos posteriores, como RemoteRead, usan el identificador de contexto como un puntero in.

Además del procedimiento remoto que inicializa el identificador de contexto, la interfaz debe contener un procedimiento que libere el contexto del servidor y establezca el identificador de contexto en **null**. En el ejemplo anterior, la función RemoteClose realiza esta operación.

 

 