---
title: atributo predeterminado
description: El atributo \ default \ indica que la interfaz o la dispinterface, definidas dentro de una coclase, representa la interfaz de programación predeterminada. Este atributo está pensado para que lo usen los lenguajes de macros.
ms.assetid: 66769dff-60a0-4e6e-9357-c4339c0bfa3f
keywords:
- valor predeterminado del atributo MIDL
topic_type:
- apiref
api_name:
- default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2171515bffc41abf2b5fe9a25826c2a71d3939c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487586"
---
# <a name="default-attribute"></a>atributo predeterminado

El atributo **\[ \] default** indica que la [**interfaz**](interface.md) o la [**dispinterface**](dispinterface.md), definidas dentro de una [**coclase**](coclass.md), representa la interfaz de programación predeterminada. Este atributo está pensado para que lo usen los lenguajes de macros.

``` syntax
[
    uuid(uuid-number) 
    [, attribute-list]
] 
coclass coclass-name
{
    [ default [, optional-interface-attribute] ]; 
    interface | dispinterface interface-name;
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*UUID-número* 
</dt> <dd>

Especifica un número de identificación único universal para la [**coclase**](coclass.md).

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica atributos de [**coclase**](coclass.md) adicionales. Separe varios atributos con comas.

</dd> <dt>

*nombre de coclase* 
</dt> <dd>

Especifica el nombre por el que otros componentes de software pueden hacer referencia a esta [**coclase**](coclass.md).

</dd> <dt>

*Optional-interface-Attribute* 
</dt> <dd>

El **\[** atributo de [**origen**](source.md) **\]** , que especifica que una interfaz o dispinterface es saliente, es el único otro atributo que se puede utilizar aquí.

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una [**coclase**](coclass.md) puede tener como máximo dos miembros **\[ predeterminados \]** . Uno representa la interfaz de salida (origen) o la dispinterface, y el otro representa la interfaz (receptor) entrante o dispinterface. Si no se especifica el atributo **\[ default \]** para ningún miembro de la **coclase** o **cotype**, los primeros miembros salientes y entrantes que no tienen el **\[** atributo [**Restricted**](restricted.md) **\]** se tratan como valores predeterminados.

### <a name="flags"></a>Marcas

IMPLTYPEFLAG \_ FDEFAULT

## <a name="examples"></a>Ejemplos

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello Class"),appobject
]  
coclass Hello
{
    [default] interface IHello:IUnknown;
    interface IDispatch;
};
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**coclase**](coclass.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Restrict**](restricted.md)
</dt> <dt>

[**fuentes**](source.md)
</dt> </dl>

 

 