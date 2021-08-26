---
title: La midl_user_free de datos
description: Los desarrolladores de RPC deben proporcionar la función gratuita de usuario \_ \_ midl.
ms.assetid: 5e940e93-bdd4-48cc-b84e-654637699719
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd6ca52635da5bedb60fdc7f94165ad9c888c030d5fe3340c53dfc970a90ff49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080835"
---
# <a name="the-midl_user_free-function"></a>La función gratuita del \_ \_ usuario midl

Los **\_ desarrolladores \_ de** RPC deben proporcionar la función gratuita de usuario midl. Asigna memoria para los códigos auxiliares RPC y las rutinas de biblioteca. La **función gratuita del \_ \_ usuario midl** debe coincidir con el siguiente prototipo:

``` syntax
void __RPC_USER midl_user_free(void * pBuffer);
```

El *parámetro pBuffer* especifica un puntero a la memoria que se va a liberar. Tanto la aplicación cliente como la aplicación de servidor deben implementar la función gratuita de usuario **midl \_ \_** a menos que esté compilando en modo de compatibilidad con OSF ([**/osf).**](/windows/desktop/Midl/-osf) La **función gratuita \_ de \_ usuario midl** debe ser capaz de liberar todo el almacenamiento asignado por [**midl \_ user \_ allocate**](the-midl-user-allocate-function.md).

Las aplicaciones y los códigos auxiliares **llaman al usuario midl \_ \_ libremente** cuando se trabaja con objetos asignados:

-   La aplicación de servidor debe llamar al usuario **midl \_ \_** libre para liberar memoria asignada por la aplicación, como al eliminar un nodo de datos asignado dinámicamente.
-   El código auxiliar del servidor llama al usuario **\_ \_ midl** libremente para liberar memoria en el servidor después de serializar todos los \[ argumentos de salida, en los argumentos , out y el valor devuelto \] de la \[ \] \[ \] función.

Por ejemplo, rpc Windows programa de ejemplo que muestra "Hello, world" implementa el usuario **midl \_ \_** libre en términos de la función C gratis:


```C++
void __RPC_USER midl_user_free(void __RPC_FAR * p)
{
    free(p);
}
```



> [!Note]  
> Si el paquete RpcSs está habilitado (por ejemplo, como resultado de usar el atributo enable allocate), el programa de servidor debe usar \[ [**\_**](/windows/desktop/Midl/enable-allocate) \] [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) para liberar memoria. Para obtener más información, vea [RpcSs Memory Management Package](rpcss-memory-management-package.md).

 

 

 