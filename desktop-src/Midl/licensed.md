---
title: atributo con licencia
description: El atributo \licensed\ indica que la coclase a la que se aplica tiene licencia y se deben crear instancias mediante IClassFactory2.
ms.assetid: c4789ea2-8ff6-423e-8b69-22a7a5392854
keywords:
- atributo con licencia MIDL
topic_type:
- apiref
api_name:
- licensed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f24d8b6136cab86615e74838737bbda543b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159509"
---
# <a name="licensed-attribute"></a>atributo con licencia

El **\[ atributo \]** con licencia indica que la [**coclase**](coclass.md) a la que se aplica tiene licencia y se deben crear instancias mediante [**IClassFactory2.**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2)

``` syntax
[
    licensed
    [ , attribute-list ] 
]
coclass classname 
{
  coclass-definition
};
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*attribute-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la [**instrucción coclass.**](coclass.md) Los atributos **de la coclase** permitidos **\[** [**son helpstring**](helpstring.md) **\]** , **\[** [**helpcontext**](helpcontext.md), **\]** **\[ licensed \]**, **\[** [**version**](version.md) **\]** , **\[** [**control**](control.md) **\]** y **\[** [**hidden.**](hidden.md) **\]**

</dd> <dt>

*classname* 
</dt> <dd>

Especifica el nombre por el que se conoce el objeto de componente en la biblioteca de tipos.

</dd> <dt>

*coclass-definition* 
</dt> <dd>

Especifica las instrucciones que son la definición [**de la clase conjunta.**](coclass.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las licencias son una característica de COM que proporciona control sobre la creación de objetos. Los objetos con licencia solo los pueden crear los clientes que están autorizados para usarlos. Las licencias se implementan en COM mediante la [**interfaz IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) y la compatibilidad con una clave de licencia que se puede pasar en tiempo de ejecución.

### <a name="flags"></a>Marcas

TYPEFLAG \_ FLICENSED

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    licensed, 
    helpstring("A meaningfulcomment"
]
coclass MyClass
{
    // coclass definition statements
};
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**coclase**](coclass.md)
</dt> <dt>

[Contenido de una biblioteca de tipos](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**Control**](control.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**Oculto**](hidden.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**version**](version.md)
</dt> </dl>

 

 