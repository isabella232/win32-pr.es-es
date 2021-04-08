---
title: defaultbind (atributo)
description: El atributo \ defaultbind \ indica la única propiedad enlazable que mejor representa el objeto.
ms.assetid: 8cf0922a-3d7c-404d-b4fd-edbd772987bf
keywords:
- defaultbind (atributo) MIDL
topic_type:
- apiref
api_name:
- defaultbind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 518c11da8d5f9b0762843c5b69292562a94b80c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077725"
---
# <a name="defaultbind-attribute"></a>defaultbind (atributo)

El atributo **\[ defaultbind \]** indica la única propiedad enlazable que representa mejor el objeto.

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

*interfaz-atributo-lista* 
</dt> <dd>

Especifica una lista de uno o más atributos que se aplican a la interfaz en conjunto. Cuando dos o más atributos de interfaz están presentes, deben separarse con comas.

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica una lista de uno o más atributos que se aplican a la función. Cuando dos o más atributos de interfaz están presentes, deben separarse con comas.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función a la que se aplicará el atributo **\[ defaultbind \]** .

</dd> <dt>

*params* 
</dt> <dd>

Lista de parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las propiedades que tienen el atributo **\[ defaultbind \]** también deben tener el **\[** atributo [**enlazable**](bindable.md) **\]** . Solo una propiedad de una interfaz o dispinterface puede tener el atributo **\[ defaultbind \]** .

Este atributo lo usan los contenedores que tienen un modelo de usuario que implica un enlace a un objeto en lugar de enlazar a una propiedad de un objeto. Un objeto puede admitir el enlace de datos pero no tiene este atributo.

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

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 