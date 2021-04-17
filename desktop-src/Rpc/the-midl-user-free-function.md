---
title: La función midl_user_free
description: Los \_ desarrolladores de \_ RPC deben proporcionar la función gratuita de usuario de MIDL.
ms.assetid: 5e940e93-bdd4-48cc-b84e-654637699719
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4713ed05173b709780b6496f233051fa3adddff8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421324"
---
# <a name="the-midl_user_free-function"></a>La \_ función gratuita de usuario de MIDL \_

Los desarrolladores de RPC deben proporcionar la función **\_ \_ gratuita de usuario de MIDL** . Asigna memoria para el código auxiliar RPC y las rutinas de biblioteca. La **función \_ \_ gratuita de usuario de MIDL** debe coincidir con el prototipo siguiente:

``` syntax
void __RPC_USER midl_user_free(void * pBuffer);
```

El parámetro *pBuffer* especifica un puntero a la memoria que se va a liberar. Tanto la aplicación cliente como la aplicación de servidor deben implementar la función **\_ \_ gratuita de usuario de MIDL** a menos que esté compilando en modo de compatibilidad de OSF ([**/OSF**](/windows/desktop/Midl/-osf)). La **función \_ \_ gratuita de usuario de MIDL** debe ser capaz de liberar todo el almacenamiento asignado por el usuario de la [**\_ \_ asignación de MIDL**](the-midl-user-allocate-function.md).

Las aplicaciones y los códigos auxiliares llaman al **usuario de MIDL \_ \_ gratis** cuando se trabaja con objetos asignados:

-   La aplicación de servidor debe llamar al **usuario de MIDL \_ \_** para liberar memoria asignada por la aplicación, como cuando se elimina un nodo de datos asignado dinámicamente.
-   El código auxiliar del servidor llama **\_ \_ gratuitamente al usuario de MIDL** para liberar memoria en el servidor después de calcular las referencias de todos los \[ \] argumentos de salida, \[ en \] , \[ los argumentos de salida \] y el valor devuelto de la función.

Por ejemplo, el programa de ejemplo RPC de Windows que muestra "Hello, World" implementa de forma gratuita el **usuario de MIDL \_ \_** en términos de la función de C:


```C++
void __RPC_USER midl_user_free(void __RPC_FAR * p)
{
    free(p);
}
```



> [!Note]  
> Si el paquete RpcSs está habilitado (por ejemplo, como resultado de usar el \[ atributo [**enable \_ allocate**](/windows/desktop/Midl/enable-allocate) \] ), el programa de servidor debe usar [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) para liberar memoria. Para obtener más información, consulte el [paquete de administración de memoria RPCSS](rpcss-memory-management-package.md).

 

 

 