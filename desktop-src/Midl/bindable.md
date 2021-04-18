---
title: bindable (atributo)
description: El atributo \ Bindable \ indica que la propiedad admite el enlace de datos.
ms.assetid: ba09096d-a2f7-4958-827c-0fba19ded26f
keywords:
- MIDL del atributo enlazable
topic_type:
- apiref
api_name:
- bindable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33911ba5ff55ef5e3dd377613dd98532ecd97486
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105685698"
---
# <a name="bindable-attribute"></a>bindable (atributo)

El atributo **\[ Bindable \]** indica que la propiedad admite el enlace de datos.

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

*interfaz-atributo-lista* 
</dt> <dd>

Especifica una lista de cero o más atributos IDL que se aplican a la interfaz en conjunto. Cuando dos o más atributos de interfaz están presentes, deben separarse con comas.

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica cero o más atributos que se aplican al prototipo de función para una propiedad o un método en una [**interfaz**](interface.md) o [**dispinterface**](dispinterface.md). Los atributos siguientes son válidos: [**\[ \] HelpString**](helpstring.md), [**\[ \] HelpContext**](helpcontext.md), [**\[ String \]**](string.md), [**\[ defaultbind \]**](defaultbind.md), [**\[ displaybind \]**](displaybind.md), [**\[ immediatebind \]**](immediatebind.md), [**\[ propget \]**](propget.md), [**\[ PROPPUT \]**](propput.md), [**\[ PROPPUTREF \]**](propputref.md)y [**\[ vararg \]**](vararg.md). Si se especifica **vararg** , el último parámetro debe ser una matriz segura de tipo Variant. Separe varios atributos con comas.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función a la que se aplicará el atributo **\[ enlazable \]** .

</dd> <dt>

*params* 
</dt> <dd>

Lista de parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al admitir el enlace de datos, el atributo **\[ enlazable \]** permite al cliente recibir una notificación cada vez que una propiedad ha cambiado de valor. (Si desea que el cliente reciba notificaciones de cambios inminentes en una propiedad, use el atributo [**\[ requestedit \]**](requestedit.md) ).

Dado que el atributo **\[ enlazable \]** hace referencia a la propiedad como un todo, se debe especificar dondequiera que se defina la propiedad. Por lo tanto, debe especificar el atributo en la función de acceso a propiedades y en la función de configuración de propiedades.

### <a name="flags"></a>Marcas

FUNCFLAG \_ FBINDABLE, VARFLAG \_ FBINDABLE

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

[**dispinterface**](dispinterface.md)
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

[**interfaz**](interface.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**PROPPUT**](propput.md)
</dt> <dt>

[**PROPPUTREF**](propputref.md)
</dt> <dt>

[**requestedit**](requestedit.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**vararg**](vararg.md)
</dt> </dl>

 

 