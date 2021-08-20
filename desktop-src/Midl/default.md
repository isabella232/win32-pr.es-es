---
title: atributo predeterminado
description: El atributo \ default\ indica que la interfaz o dispinterface, definida dentro de una coclase, representa la interfaz de programación predeterminada. Este atributo está pensado para su uso por los lenguajes de macro.
ms.assetid: 66769dff-60a0-4e6e-9357-c4339c0bfa3f
keywords:
- atributo predeterminado MIDL
topic_type:
- apiref
api_name:
- default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea717048a89c626ef19d5b1c41fcd558a163f7b4ade9c05eee0e3ea362d50ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013943"
---
# <a name="default-attribute"></a>atributo predeterminado

El **\[ atributo \]** predeterminado Indica que la [**interfaz**](interface.md) o [**dispinterface**](dispinterface.md), definida dentro de una [**coclase**](coclass.md), representa la interfaz de programación predeterminada. Este atributo está pensado para su uso por los lenguajes de macro.

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

*uuid-number* 
</dt> <dd>

Especifica un número de identificación único universal para la [**coclase**](coclass.md).

</dd> <dt>

*attribute-list* 
</dt> <dd>

Especifica atributos de [**coclase adicionales.**](coclass.md) Separe varios atributos con comas.

</dd> <dt>

*coclass-name* 
</dt> <dd>

Especifica el nombre por el que otros componentes de software pueden hacer referencia a esta [**coclase**](coclass.md).

</dd> <dt>

*optional-interface-attribute* 
</dt> <dd>

El atributo de origen, que especifica que una interfaz o dispinterface es saliente, es el único atributo **\[** [](source.md) **\]** que se puede usar aquí.

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una [**coclase**](coclass.md) puede tener como máximo dos **\[ miembros predeterminados. \]** Una representa la interfaz saliente (origen) o dispinterface, y la otra representa la interfaz entrante (receptor) o dispinterface. Si no **\[ se \]** especifica el atributo predeterminado para ningún miembro de la **coclase** o **el cotipo**, los primeros miembros salientes y entrantes que no tienen el atributo restringido se tratan como valores **\[** [](restricted.md) **\]** predeterminados.

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

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Restringido**](restricted.md)
</dt> <dt>

[**Fuente**](source.md)
</dt> </dl>

 

 