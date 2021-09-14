---
title: displaybind (atributo)
description: El atributo \ displaybind\ indica una propiedad que se debe mostrar al usuario como enlazable.
ms.assetid: 047a58b2-3ae2-437a-992f-a9d1541decbe
keywords:
- atributo displaybind MIDL
topic_type:
- apiref
api_name:
- displaybind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f015954a7b1fe07d4ecf61e9a4ba4da4c932e65c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159613"
---
# <a name="displaybind-attribute"></a>displaybind (atributo)

El **\[ atributo \] displaybind** indica una propiedad que se debe mostrar al usuario como enlazable.

``` syntax
[
  [interface-attribute-list]
]
interface | dispinterface interface-name
{
    [bindable, displaybind [ , attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Especifica una lista opcional de atributos de interfaz.

</dd> <dt>

*interface-name* 
</dt> <dd>

Nombre de la interfaz.

</dd> <dt>

*attribute-list* 
</dt> <dd>

Especifica una lista de uno o varios atributos, separados por comas, que se aplican al tipo de valor devuelto de función.

</dd> <dt>

*returntype* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre de la función a la que se aplicará el atributo **\[ displaybind. \]**

</dd> <dt>

*params* 
</dt> <dd>

Lista de parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las propiedades que tienen **\[ el atributo displaybind \]** también deben tener el atributo **\[** [**enlazable.**](bindable.md) **\]** Un objeto puede admitir el enlace de datos, pero no tiene este atributo.

### <a name="flags"></a>Marcas

FUNCFLAG \_ FDISPLAYBIND, VARFLAG \_ FDISPLAYBIND

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, defaultbind, 
         displaybind] long Size(void);

        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 