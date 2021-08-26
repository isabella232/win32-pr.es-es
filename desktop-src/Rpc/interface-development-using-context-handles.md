---
title: Desarrollo de interfaces mediante identificadores de contexto
description: Normalmente, se crea un identificador de contexto especificando el atributo \ context handle\ en una \_ definición de tipo en el archivo IDL.
ms.assetid: e4caf91f-f92d-4aef-a20f-0a3073230640
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e65e36384bda3d81526d5891eca92a77a67402e7cd3aa7af8b61e061a9d3b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020475"
---
# <a name="interface-development-using-context-handles"></a>Desarrollo de interfaces mediante identificadores de contexto

Normalmente, se crea un identificador de contexto especificando el atributo \[ [**de identificador \_ de**](/windows/desktop/Midl/context-handle) \] contexto en una definición de tipo en el archivo IDL. La definición de tipo también especifica implícitamente una rutina de ejecución de contexto, que debe proporcionar. Si la comunicación entre el cliente y el servidor se interrumpe, el tiempo de ejecución del servidor invoca esta rutina para realizar cualquier limpieza necesaria. Para obtener más información sobre las rutinas de ejecución de contexto, vea [Rutina de ejecución de contexto de servidor](server-context-run-down-routine.md).

Una interfaz que usa un identificador de contexto debe tener un identificador de enlace para el enlace inicial, que debe tener lugar antes de que el servidor pueda devolver un identificador de contexto. Puede usar un identificador de enlace automático, implícito o explícito para crear el enlace y establecer el contexto.

Un identificador de contexto debe ser [ * *del tipo void \** _](/windows/desktop/Midl/void) o un tipo que se resuelve en _ [*void \** *](/windows/desktop/Midl/void). El programa de servidor lo convierte al tipo requerido.

> [!Note]  
> Se desaconseja el uso de en , para los parámetros de identificador de contexto, excepto para \[ [](/windows/desktop/Midl/in) [](/windows/desktop/Midl/out-idl) \] las rutinas que cierran los identificadores de contexto. Si el contexto controla los parámetros marcados en , se usa out, no pase un identificador de contexto NULL o no inicializado del cliente \[ [](/windows/desktop/Midl/in) [](/windows/desktop/Midl/out-idl) \] al servidor.  En **su lugar,** se debe pasar un puntero NULL a un identificador de contexto. Tenga en cuenta que los parámetros de identificador de contexto \[ marcados [**en**](/windows/desktop/Midl/in) no \] aceptan **punteros NULL.**

 

El fragmento siguiente de una definición de interfaz de ejemplo muestra cómo una aplicación distribuida puede usar un identificador de contexto para tener un servidor abierto y actualizar un archivo de datos para cada cliente.

La interfaz debe contener una llamada a procedimiento remoto para inicializar el identificador y establecerlo en un valor distinto **de NULL.** En este ejemplo, la función RemoteOpen realiza esta operación. Especifica el identificador de contexto con un \[ [**atributo direccional**](/windows/desktop/Midl/out-idl) \] out. Como alternativa, puede devolver el identificador de contexto como valor devuelto del procedimiento. Sin embargo, en este ejemplo, pasaremos el identificador de contexto a través de la lista de parámetros.

En este ejemplo, la información de contexto es un identificador de archivo. Realiza un seguimiento de la ubicación actual en el archivo. La interfaz empaqueta el identificador de archivo como un identificador de contexto y lo pasa como un parámetro a las llamadas a procedimiento remoto. Una estructura contiene el nombre de archivo y el identificador de archivo.

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

La función RemoteOpen crea un identificador de contexto válido que **no** es nulo. Pasa el identificador de contexto al cliente. Las llamadas a procedimientos remotos posteriores, como RemoteRead, usan el identificador de contexto como un puntero in.

Además del procedimiento remoto que inicializa el identificador de contexto, la interfaz debe contener un procedimiento que libera el contexto del servidor y establece el identificador de contexto en **NULL.** En el ejemplo anterior, la función RemoteClose realiza esta operación.

 

 