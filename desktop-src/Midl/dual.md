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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159610"
---
# <a name="dual-attribute"></a>atributo dual

El **atributo** dual identifica una interfaz que expone propiedades y métodos a través [**de IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) y directamente a través de VTBL.

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

*uuid-number* 
</dt> <dd>

Especifica un número de identificación único universal para la interfaz

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Especifica una lista de cero o más atributos MIDL adicionales.

</dd> <dt>

*interface-name* 
</dt> <dd>

Nombre de la interfaz a la que **se** aplicará el atributo dual.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las interfaces identificadas por **el atributo dual** deben ser compatibles con Automation y derivarse de [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) Este atributo no se permite en interfaces dispinterface.

El **atributo** dual crea una interfaz que es una interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) y una interfaz de Modelo de objetos componentes (COM). Las siete primeras entradas de VTBL para una interfaz dual son los siete miembros de **IDispatch** y las entradas restantes son para el acceso directo a los miembros de la interfaz dual. Todos los parámetros y tipos de valor devuelto especificados para los miembros de una interfaz dual deben ser tipos compatibles con Automation.

Todos los miembros de una interfaz dual deben pasar un valor HRESULT como el valor devuelto de la función. Los miembros, como las funciones de accessor de propiedad, que necesitan devolver otros valores, deben especificar el último parámetro como [**out**](out-idl.md), [**retval**](retval.md), que indica un parámetro de salida que devuelve el valor de la función. Además, los miembros que necesitan admitir varias configuraciones regionales deben pasar un [**parámetro lcid.**](lcid.md)

Una interfaz dual proporciona la velocidad del enlace VTBL directo y la flexibilidad del [**enlace IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) Por esta razón, se recomiendan interfaces duales siempre que sea posible.

> [!Note]  
> Si la aplicación accede a  los datos del objeto mediante la conversión del puntero this dentro de la llamada de interfaz, debe comprobar los punteros VTBL del objeto con sus propios punteros VTBL para asegurarse de que está conectado al proxy adecuado.

 

Especificar **dual** en una interfaz implica que la interfaz es compatible con Automation y, por tanto, hace que se establezcan las marcas TYPEFLAG FDUAL y \_ TYPEFLAG \_ FOLTOMATION.

### <a name="flags"></a>Marcas

TYPEFLAG \_ FDUAL, TYPEFLAG \_ FOLTOMTOMATION

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

[**Interfaz**](interface.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Retval**](retval.md)
</dt> </dl>

 

 