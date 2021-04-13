---
title: midl_user_free atributo)
description: La función gratuita de usuario de MIDL la \_ \_ proporcionan las aplicaciones de cliente y servidor para desasignar la memoria asignada dinámicamente.
ms.assetid: b5d8f133-ddd9-4b92-8540-611a03835be0
keywords:
- midl_user_free el atributo MIDL
topic_type:
- apiref
api_name:
- midl_user_free
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53819035f700a948c9ca45c565310d7796516147
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358896"
---
# <a name="midl_user_free-attribute"></a>\_atributo Free de usuario de MIDL \_

La **función \_ \_ gratuita de usuario de MIDL** la proporcionan las aplicaciones de cliente y servidor para desasignar la memoria asignada dinámicamente.

``` syntax
void __RPC_API midl_user_free(void __RPC_FAR * p);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*m* 
</dt> <dd>

Puntero al bloque de memoria que se va a liberar.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tanto la aplicación cliente como la aplicación de servidor deben implementar la función **\_ \_ gratuita de usuario de MIDL** , a menos que esté compilando en modo de compatibilidad de OSF ([**/OSF**](-osf.md)). La **función \_ \_ gratuita de usuario de MIDL** debe ser capaz de liberar todo el almacenamiento asignado por el usuario de la [**\_ \_ asignación de MIDL**](/windows/desktop/Rpc/the-midl-user-allocate-function).

Las aplicaciones y los códigos auxiliares llaman al **usuario de MIDL \_ \_ gratis** al tratar con objetos a los que hacen referencia los punteros:

-   La aplicación de servidor debe llamar al **usuario de MIDL \_ \_ Free** para liberar memoria asignada por aplicación € ", por ejemplo, al eliminar un nodo especificado.
-   El código auxiliar del servidor llama **\_ \_ gratuitamente al usuario de MIDL** para liberar memoria en el servidor después de calcular las referencias de todos los **\[** [](out-idl.md) **\]** argumentos de salida, **\[** [**en**](in.md), los argumentos de **salida \]** y el valor devuelto.

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

[**matrices**](arrays-1.md)
</dt> <dt>

[Matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Atributos array y Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**de**](in.md)
</dt> <dt>

[**\_asignación de usuarios de MIDL \_**](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> <dt>

[**espeficarse**](unique.md)
</dt> </dl>

 

 