---
title: midl_user_allocate atributo)
description: La función de asignación de usuarios de MIDL \_ \_ es una función que proporcionan las aplicaciones cliente y servidor para asignar memoria.
ms.assetid: 0eaf6df5-791d-4f6d-8f49-cc1ce64e7ab4
keywords:
- midl_user_allocate el atributo MIDL
topic_type:
- apiref
api_name:
- midl_user_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4be10c5e1c7073afb3abf359c3ec2fb79a4335b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358949"
---
# <a name="midl_user_allocate-attribute"></a>atributo de asignación de \_ usuarios de MIDL \_

La función de **\_ \_ asignación de usuarios de MIDL** es una función que proporcionan las aplicaciones cliente y servidor para asignar memoria.

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate (size_t cBytes);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*cBytes* 
</dt> <dd>

Especifica el recuento de bytes que se van a asignar.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las aplicaciones cliente y las aplicaciones de servidor deben implementar la función de **\_ \_ asignación de usuarios de MIDL** , a menos que se esté compilando en modo de compatibilidad de OSF ([**/OSF**](-osf.md)). Las aplicaciones y los códigos auxiliares generados llaman a la **\_ \_ asignación de usuarios de MIDL** al tratar con objetos a los que hacen referencia los punteros:

-   La aplicación de servidor debe llamar a **MIDL \_ User \_ allocate** para asignar memoria para aplicación € ", por ejemplo, al crear un nuevo nodo.
-   El código auxiliar del servidor llama a la **\_ \_ asignación de usuarios de MIDL** al desserializar los datos señalados en el espacio de direcciones del servidor.
-   El código auxiliar de cliente llama a la **\_ \_ asignación de usuario de MIDL** al quitar las referencias de datos del servidor al que hace referencia un puntero de [**salida**](out-idl.md) . Tenga en cuenta que para **\[** [](in.md) **\]** los punteros in, **\[ out \]** y **\[** [**Unique**](unique.md) **\]** , el código auxiliar de cliente llama a la **\_ \_ asignación de usuario de MIDL** solo si el valor de puntero **\[ único \]** era **null** en la entrada y cambia a un valor distinto de **null** durante la llamada. Si el puntero **\[ \] único** no era **null** en la entrada, el código auxiliar del cliente escribe los datos asociados en la memoria existente.

Si el usuario de la **\_ \_ asignación de MIDL** no puede asignar memoria, debe devolver un puntero **nulo** .

Se recomienda que la **\_ \_ asignación de usuarios de MIDL** devuelva un puntero de 8 bytes alineado.

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

[**matrices**](arrays-1.md)
</dt> <dt>

[Matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Atributos array y Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**de**](in.md)
</dt> <dt>

[**usuario de MIDL \_ \_ gratis**](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**espeficarse**](unique.md)
</dt> </dl>

 

 