---
title: atributo dual
description: El atributo dual identifica una interfaz que expone propiedades y métodos a través de IDispatch y directamente a través de VTBL.
ms.assetid: 1c214f10-57eb-4a05-99a8-a09770666a74
keywords:
- MIDL de atributo dual
topic_type:
- apiref
api_name:
- dual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39a9e44de464f58fd1ffc0606551b9a0203ae9e9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995236"
---
# <a name="dual-attribute"></a>atributo dual

El atributo **dual** identifica una interfaz que expone propiedades y métodos a través de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) y directamente a través de VTBL.

``` syntax
[
    uuid(uuid-number), 
    oleautomation,
    dual 
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*UUID-número* 
</dt> <dd>

Especifica un número de identificación único universal para la interfaz.

</dd> <dt>

*opcional-Attribute-List* 
</dt> <dd>

Especifica una lista de cero o más atributos MIDL adicionales.

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

Nombre de la interfaz a la que se aplicará el atributo **dual** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las interfaces identificadas por el atributo **dual** deben ser compatibles con la automatización y derivarse de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch). Este atributo no se permite en interfaces dispinterface.

El atributo **dual** crea una interfaz que es una interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) y una interfaz del modelo de objetos componentes (com). Las siete primeras entradas de VTBL para una interfaz dual son los siete miembros de **IDispatch** y las entradas restantes son para el acceso directo a los miembros de la interfaz dual. Todos los parámetros y tipos devueltos especificados para los miembros de una interfaz dual deben ser tipos compatibles con la automatización.

Todos los miembros de una interfaz dual deben pasar un HRESULT como el valor devuelto de la función. Los miembros, como las funciones de descriptor de acceso de propiedades, que necesitan devolver otros valores, deben especificar el último parámetro como [**out**](out-idl.md), [**retval**](retval.md), que indica un parámetro de salida que devuelve el valor de la función. Además, los miembros que deben admitir varias configuraciones regionales deben pasar un parámetro [**LCID**](lcid.md) .

Una interfaz dual proporciona tanto la velocidad del enlace VTBL directo como la flexibilidad del enlace [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Por esta razón, siempre que sea posible, se recomienda usar interfaces duales.

> [!Note]  
> Si la aplicación obtiene acceso a los datos de objeto mediante la conversión del puntero *this* dentro de la llamada de interfaz, debe comprobar los punteros VTBL en el objeto con sus propios punteros VTBL para asegurarse de que está conectado al proxy adecuado.

 

Especificar **dual** en una interfaz implica que la interfaz es compatible con la automatización y, por consiguiente, hace que \_ se establezcan las marcas TYPEFLAG FDUAL y TYPEFLAG \_ FOLEAUTOMATION.

### <a name="flags"></a>Marcas

TYPEFLAG \_ FDUAL, TYPEFLAG \_ FOLEAUTOMATION

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    oleautomation, dual
]
interface IHello : IDispatch
{
    //Diverse properties and methods defined here.
};
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**interfaz**](interface.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 