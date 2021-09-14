---
title: midl_user_free atributo
description: Las aplicaciones cliente y servidor proporcionan la función gratuita de usuario midl \_ \_ para desasignar la memoria asignada dinámicamente.
ms.assetid: b5d8f133-ddd9-4b92-8540-611a03835be0
keywords:
- midl_user_free atributo MIDL
topic_type:
- apiref
api_name:
- midl_user_free
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53819035f700a948c9ca45c565310d7796516147
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159488"
---
# <a name="midl_user_free-attribute"></a>Midl \_ user \_ free attribute

Las **aplicaciones cliente \_ \_ y** servidor proporcionan la función gratuita de usuario midl para desasignar la memoria asignada dinámicamente.

``` syntax
void __RPC_API midl_user_free(void __RPC_FAR * p);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*P* 
</dt> <dd>

Puntero al bloque de memoria que se va a liberar.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tanto la aplicación cliente como la aplicación de servidor deben implementar la función gratuita de usuario **midl, \_ \_** a menos que se esté compilando en modo de compatibilidad con OSF ([**/osf).**](-osf.md) La **función gratuita de usuario \_ \_ midl** debe ser capaz de liberar todo el almacenamiento asignado por [**midl user \_ \_ allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function).

Las aplicaciones y los códigos auxiliares **llaman a midl \_ user \_ free** cuando se trabaja con objetos a los que hacen referencia los punteros:

-   La aplicación de servidor debe llamar al usuario **midl \_ \_** libremente para liberar memoria asignada por la aplicación, por ejemplo, al eliminar un nodo especificado.
-   El código auxiliar del servidor llama al usuario **midl \_ \_** libremente para liberar memoria en el servidor después de serializar todos los **\[** [](out-idl.md) **\]** argumentos de salida, en **\[** [](in.md) **\]** , argumentos out y el valor devuelto.

## <a name="examples"></a>Ejemplos


```C++
#include <windows.h>

void __RPC_API midl_user_free(void __RPC_FAR * p) 
{ 
    free(p); 
}
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Matrices**](arrays-1.md)
</dt> <dt>

[Matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Atributos de matriz Sized-Pointer matriz](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**En**](in.md)
</dt> <dt>

[**midl \_ user \_ allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Único**](unique.md)
</dt> </dl>

 

 