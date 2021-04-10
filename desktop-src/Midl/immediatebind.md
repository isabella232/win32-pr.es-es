---
title: immediatebind (atributo)
description: El atributo \ immediatebind \ indica que se notificará inmediatamente a la base de datos todos los cambios en una propiedad de un objeto enlazado a datos.
ms.assetid: 1c08ddca-e273-43b3-a8f6-ed7f552e4e0e
keywords:
- immediatebind (atributo) MIDL
topic_type:
- apiref
api_name:
- immediatebind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8a797514c15f8d4c46bb6161946d5d0b6bd10b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104270839"
---
# <a name="immediatebind-attribute"></a>immediatebind (atributo)

El atributo **\[ immediatebind \]** indica que se notificará inmediatamente a la base de datos todos los cambios en una propiedad de un objeto enlazado a datos.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, immediatebind[, optional-attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*interfaz-atributo-lista* 
</dt> <dd>

Especifica una lista de uno o más atributos que se aplican a la interfaz en conjunto.

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

Especifica el nombre de la [**interfaz**](interface.md) o [**dispinterface**](dispinterface.md).

</dd> <dt>

*opcional-Attribute-List* 
</dt> <dd>

Cero o más atributos de función.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función en el archivo IDL.

</dd> <dt>

*params* 
</dt> <dd>

Cero o más parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ immediatebind \]** permite a los controles diferenciar entre las propiedades que necesitan notificar a la base de datos todos los cambios y las que no lo hacen. Por ejemplo, cada cambio en un control CheckBox debe enviarse inmediatamente a la base de datos subyacente, incluso si el control no ha perdido el foco. Sin embargo, para un control ListBox, se produce un cambio cada vez que se resalta una selección diferente. Notificar a la base de datos un cambio antes de que el control pierda el foco sería ineficaz e innecesario. El atributo **\[ immediatebind \]** permite especificar, estableciendo el bit immediatebind, propiedades individuales en un formulario cuyos cambios se deben notificar inmediatamente.

Las propiedades que tienen el atributo **\[ immediatebind \]** también deben tener el **\[** atributo [**enlazable**](bindable.md) **\]** .

### <a name="flags"></a>Marcas

FUNCFLAG \_ FIMMEDIATEBIND, VARFLAG \_ FIMMEDIATEBIND

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, immediatebind] long Size(void);

        [id(1), propput, bindable, 
         immediatebind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**interfaz**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 