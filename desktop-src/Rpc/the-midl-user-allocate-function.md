---
title: La función midl_user_allocate
description: La \_ \_ función de asignación de usuarios de MIDL es un procedimiento que deben proporcionar los desarrolladores de aplicaciones RPC.
ms.assetid: 3def405c-da05-4cce-9dc4-499864a0de6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b2e3196de79992f5856b7117b25f05ad782d26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149456"
---
# <a name="the-midl_user_allocate-function"></a>Función de \_ asignación de usuarios de MIDL \_

La función de **\_ \_ asignación de usuarios de MIDL** es un procedimiento que deben proporcionar los desarrolladores de aplicaciones RPC. Asigna memoria para el código auxiliar RPC y las rutinas de biblioteca. La función de **\_ \_ asignación de usuarios de MIDL** debe coincidir con el prototipo siguiente:

``` syntax
void __RPC_FAR * __RPC_USER midl_user_allocate (size_t cBytes);
```

El parámetro *cBytes* especifica el número de bytes que se van a asignar. Las aplicaciones cliente y las aplicaciones de servidor deben implementar la función de **\_ \_ asignación de usuarios de MIDL** a menos que esté compilando en modo de compatibilidad de OSF (/OSF). Las aplicaciones y los códigos auxiliares generados llaman de forma directa o indirecta a los **\_ \_ usuarios de MIDL** para administrar los objetos asignados. Por ejemplo:

-   Las aplicaciones de cliente y servidor llaman a la **\_ \_ asignación de usuarios de MIDL** para asignar memoria para la aplicación, como cuando se crea un nuevo nodo en un árbol o lista vinculada.
-   El código auxiliar del servidor llama a la **\_ \_ asignación de usuarios de MIDL** al calcular las referencias de los datos en el espacio de direcciones del servidor.
-   El código auxiliar de cliente llama a la **\_ \_ asignación de usuario de MIDL** al quitar las referencias de datos del servidor al que hace referencia un puntero de \[ salida \] . Tenga en cuenta que para \[ \] \[ \] los punteros in, out y \[ Unique \] , el código auxiliar de cliente llama a la **asignación de \_ usuario \_ de MIDL** solo si el \[ valor de \] puntero único era null en la entrada y cambia a un valor distinto de NULL durante la llamada. Si el \[ puntero único no \] era null en la entrada, el código auxiliar del cliente escribe los datos asociados en la memoria existente.

Si **el \_ usuario \_** de la asignación de MIDL no puede asignar memoria, debe devolver un puntero nulo.

La función de **\_ \_ asignación de usuarios de MIDL** debe devolver un puntero alineado de 8 bytes.

Por ejemplo, los programas de ejemplo que se proporcionan con el kit de desarrollo de software (SDK) de la plataforma implementan **MIDL \_ User \_ alloca** en términos de la función de C [**malloc**](pointers-and-memory-allocation.md):


```C++
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t cBytes)
{
    return((void __RPC_FAR *) malloc(cBytes));
}
```



> [!Note]  
> Si el paquete RpcSs está habilitado (por ejemplo, como resultado de usar el \[ atributo [**enable \_ allocate**](/windows/desktop/Midl/enable-allocate) \] ), use [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) para asignar memoria en el lado servidor. Para obtener información adicional sobre cómo \[ **Habilitar la \_ asignación** \] , vea [referencia de MIDL](/windows/desktop/Midl/midl-language-reference).

 

 

 