---
title: midl_user_allocate atributo
description: La función de asignación de usuario de nivel medio es una función que las aplicaciones \_ cliente y servidor proporcionan para asignar \_ memoria.
ms.assetid: 0eaf6df5-791d-4f6d-8f49-cc1ce64e7ab4
keywords:
- midl_user_allocate atributo MIDL
topic_type:
- apiref
api_name:
- midl_user_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4be10c5e1c7073afb3abf359c3ec2fb79a4335b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159487"
---
# <a name="midl_user_allocate-attribute"></a>atributo de \_ asignación \_ de usuario midl

La **función de \_ asignación de \_ usuario** de nivel medio es una función que las aplicaciones cliente y servidor proporcionan para asignar memoria.

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate (size_t cBytes);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*cBytes* 
</dt> <dd>

Especifica el recuento de bytes que se asignarán.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tanto las aplicaciones cliente como las aplicaciones de servidor deben implementar la función **de \_ \_** asignación de usuario de nivel medio, a menos que esté compilando en modo de compatibilidad con OSF ([**/osf).**](-osf.md) Las aplicaciones y los códigos auxiliares generados llaman a la asignación de usuario **midl \_ \_** cuando se trabaja con objetos a los que hacen referencia los punteros:

-   La aplicación de servidor debe llamar a **midl \_ user \_ allocate** para asignar memoria para la aplicación; por ejemplo, al crear un nuevo nodo.
-   El código auxiliar del servidor llama **a la asignación de \_ \_** usuario medio al desmarque de los datos apuntados en el espacio de direcciones del servidor.
-   El código auxiliar de cliente llama a la asignación de usuario **midl \_ \_** al desmarque de datos del servidor al que hace referencia un [**puntero out.**](out-idl.md) Tenga en cuenta que para en **\[** , [](in.md) **\]** **\[ \]** out y **\[** [](unique.md) **\]** punteros únicos, **\[ \]**   **\_ \_** el código auxiliar de cliente llama a midl user allocate solo si el valor de puntero único era NULL en la entrada y cambia a un valor distinto de NULL durante la llamada. Si el **\[ puntero único \]** no era NULL **en** la entrada, el código auxiliar del cliente escribe los datos asociados en la memoria existente.

Si **la \_ asignación de usuario \_ midl** no puede asignar memoria, debe devolver un **puntero NULL.**

Se recomienda que el **usuario midl \_ \_ allocate** devuelva un puntero que tiene 8 bytes alineados.

## <a name="examples"></a>Ejemplos


```C++
#include <windows.h>

void __RPC_FAR * __RPC_API midl_user_allocate(size_t cBytes) 
{ 
    return(malloc(cBytes)); 
}
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**Matrices**](arrays-1.md)
</dt> <dt>

[Matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Atributos de matriz Sized-Pointer matriz](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**En**](in.md)
</dt> <dt>

[**midl \_ user \_ free**](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Único**](unique.md)
</dt> </dl>

 

 