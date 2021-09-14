---
title: bindable (atributo)
description: El atributo \bindable\ indica que la propiedad admite el enlace de datos.
ms.assetid: ba09096d-a2f7-4958-827c-0fba19ded26f
keywords:
- ATRIBUTO enlazable MIDL
topic_type:
- apiref
api_name:
- bindable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33911ba5ff55ef5e3dd377613dd98532ecd97486
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159672"
---
# <a name="bindable-attribute"></a>bindable (atributo)

El **\[ atributo \] enlazable** indica que la propiedad admite el enlace de datos.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable[, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Especifica una lista de cero o más atributos IDL que se aplican a la interfaz en su conjunto. Cuando hay dos o más atributos de interfaz, deben estar separados por comas.

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*attribute-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican al prototipo de función para una propiedad o un método en una [**interfaz**](interface.md) o [**dispinterface**](dispinterface.md). Los atributos siguientes son válidos: [**\[ helpstring \]**](helpstring.md), [**\[ helpcontext \]**](helpcontext.md), [**\[ \] string**](string.md), [**\[ defaultbind \]**](defaultbind.md), [**\[ displaybind \]**](displaybind.md), [**\[ immediatebind \]**](immediatebind.md), [**\[ propget \]**](propget.md), [**\[ propput \]**](propput.md), [**\[ propputref \]**](propputref.md) [**\[ ylegarg \]**](vararg.md). Si **se especifica ,** el último parámetro debe ser una matriz segura de tipo VARIANT. Separe varios atributos con comas.

</dd> <dt>

*returntype* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre de la función a la que **se \[ \]** aplicará el atributo enlazable.

</dd> <dt>

*params* 
</dt> <dd>

Lista de parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al admitir el enlace de datos, el atributo **\[ enlazable \]** permite notificar al cliente cada vez que una propiedad ha cambiado el valor. (Si desea que se notifique al cliente de los cambios inminentes en una propiedad, use el [**\[ atributo requestedit). \]**](requestedit.md)

Dado que **\[ el atributo enlazable \]** hace referencia a la propiedad en su conjunto, debe especificarse siempre que se defina la propiedad. Por lo tanto, debe especificar el atributo en la función de acceso a la propiedad y en la función de configuración de propiedades.

### <a name="flags"></a>Marcas

\_FUNCFLAGBLABLE, \_ VARFLAGBLABLE

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
]
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
        [id(1), propput, bindable, 
        defaultbind, displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**defaultbind**](defaultbind.md)
</dt> <dt>

[**Dispinterface**](dispinterface.md)
</dt> <dt>

[**displaybind**](displaybind.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**immediatebind**](immediatebind.md)
</dt> <dt>

[**Interfaz**](interface.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**requestedit**](requestedit.md)
</dt> <dt>

[**Cadena**](string.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**vararg**](vararg.md)
</dt> </dl>

 

 