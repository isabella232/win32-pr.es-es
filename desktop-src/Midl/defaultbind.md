---
title: defaultbind (atributo)
description: El atributo \ defaultbind\ indica la propiedad enlazable única que mejor representa el objeto.
ms.assetid: 8cf0922a-3d7c-404d-b4fd-edbd772987bf
keywords:
- atributo defaultbind MIDL
topic_type:
- apiref
api_name:
- defaultbind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a981d0469219a32b5931507f5df6d742e84fa67e6676e44c24edfb823f521a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807301"
---
# <a name="defaultbind-attribute"></a>defaultbind (atributo)

El **\[ atributo \] defaultbind** indica la propiedad enlazable única que mejor representa el objeto.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, defaultbind [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Especifica una lista de uno o varios atributos que se aplican a la interfaz en su conjunto. Cuando hay dos o más atributos de interfaz, deben estar separados por comas.

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*attribute-list* 
</dt> <dd>

Especifica una lista de uno o varios atributos que se aplican a la función. Cuando hay dos o más atributos de interfaz, deben estar separados por comas.

</dd> <dt>

*returntype* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función a la que se aplicará el atributo **\[ defaultbind. \]**

</dd> <dt>

*params* 
</dt> <dd>

Lista de parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las propiedades que tienen **\[ el atributo \] defaultbind** también deben tener el atributo **\[** [**enlazable.**](bindable.md) **\]** Solo una propiedad de una interfaz o dispinterface puede tener el **\[ atributo defaultbind. \]**

Los contenedores que tienen un modelo de usuario que implican el enlace a un objeto en lugar de enlazar a una propiedad de un objeto usan este atributo. Un objeto puede admitir el enlace de datos, pero no tiene este atributo.

### <a name="flags"></a>Marcas

FUNCFLAG \_ FDEFAULTBIND, VARFLAG \_ FDEFAULTBIND

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, 
         defaultbind, displaybind] long Size(void);

        [id(1), propput, bindable, 
         defaultbind, displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 