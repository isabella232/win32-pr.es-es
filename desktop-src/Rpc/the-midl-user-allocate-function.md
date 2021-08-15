---
title: La midl_user_allocate función
description: La función midl user allocate es un procedimiento que deben proporcionar los desarrolladores \_ \_ de aplicaciones RPC.
ms.assetid: 3def405c-da05-4cce-9dc4-499864a0de6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8e064fc16a303660be96a4a3c47aa361c4616f54a8cb825c1fce5334543fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924254"
---
# <a name="the-midl_user_allocate-function"></a>La función midl \_ user \_ allocate

La **función midl \_ user \_ allocate** es un procedimiento que deben proporcionar los desarrolladores de aplicaciones RPC. Asigna memoria para los códigos auxiliares de RPC y las rutinas de biblioteca. La **función midl \_ user \_ allocate** debe coincidir con el siguiente prototipo:

``` syntax
void __RPC_FAR * __RPC_USER midl_user_allocate (size_t cBytes);
```

El *parámetro cBytes* especifica el número de bytes que se asignarán. Tanto las aplicaciones cliente como las aplicaciones de servidor deben implementar la función de asignación de usuario **midl \_ \_** a menos que se esté compilando en modo de compatibilidad con OSF (/osf). Las aplicaciones y los códigos auxiliares generados llaman al usuario **midl \_ \_ allocate** directa o indirectamente para administrar objetos asignados. Por ejemplo:

-   Las aplicaciones cliente y servidor llaman a **midl \_ user \_ allocate** para asignar memoria para la aplicación, por ejemplo, al crear un nuevo nodo en un árbol o una lista vinculada.
-   El código auxiliar del servidor llama **a midl \_ user \_ allocate** al desmarque los datos en el espacio de direcciones del servidor.
-   El código auxiliar de cliente llama a **midl \_ user \_ allocate** al desmarque los datos del servidor al que hace referencia un \[ puntero \] out. Tenga en cuenta que para en \[ \] , out y \[ \] \[ \] punteros únicos, **\_ \_** \[ \] el código auxiliar de cliente llama a midl user allocate solo si el valor de puntero único era NULL en la entrada y cambia a un valor distinto de NULL durante la llamada. Si el puntero único no era NULL en la entrada, el código auxiliar del cliente \[ \] escribe los datos asociados en la memoria existente.

Si **la \_ asignación de usuario \_ midl** no puede asignar memoria, debe devolver un puntero nulo.

La **función midl \_ user \_ allocate** debe devolver un puntero alineado de 8 bytes.

Por ejemplo, los programas de ejemplo proporcionados con el Kit de desarrollo de software de plataforma (SDK) implementan la asignación de usuario **midl \_ \_** en términos de la función de C [**malloc**](pointers-and-memory-allocation.md):


```C++
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t cBytes)
{
    return((void __RPC_FAR *) malloc(cBytes));
}
```



> [!Note]  
> Si el paquete RpcSs está habilitado (por ejemplo, como resultado de usar el atributo \[ [**enable \_ allocate),**](/windows/desktop/Midl/enable-allocate) \] use [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) para asignar memoria en el lado servidor. Para obtener información adicional sobre \[ **cómo habilitar la \_ asignación,** \] vea [MidL Reference](/windows/desktop/Midl/midl-language-reference).

 

 

 