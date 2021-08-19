---
title: appobject (atributo)
description: El atributo \ appobject\ identifica la coclase como un objeto de aplicación, que está asociado a una aplicación EXE completa.
ms.assetid: f4fcdf55-7431-4d66-8a46-f741c52fbe56
keywords:
- atributo appobject MIDL
topic_type:
- apiref
api_name:
- appobject
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54cbe8d5c1c7a573216ae9cb55075ba3b3766d0d8c7898233be9364488131e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808337"
---
# <a name="appobject-attribute"></a>appobject (atributo)

El **\[ atributo \] appobject** identifica la [**coclase**](coclass.md) como un objeto de aplicación, que está asociado a una aplicación EXE completa.

``` syntax
[
    uuid(uuid-number), 
    appobject 
  [, coclass-attribute-list]
]
coclass classname 
{ 
    [coclass definition]
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*uuid-number* 
</dt> <dd>

Especifica un número de identificación único universal para la [**coclase**](coclass.md).

</dd> <dt>

*coclass-attribute-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la [**instrucción coclass.**](coclass.md) Los atributos **de la coclase** permitidos [**\[ son \] helpstring**](helpstring.md), [**\[ helpcontext \]**](helpcontext.md), [**\[ licensed \]**](licensed.md), [**\[ version \]**](version.md), [**\[ control \]**](control.md)y [**\[ hidden. \]**](hidden.md)

</dd> <dt>

*classname* 
</dt> <dd>

Especifica el nombre por el que se conoce el objeto de componente en la biblioteca de tipos.

</dd> <dt>

*definición de la coclase* 
</dt> <dd>

Especifica las instrucciones que son la definición [**de la clase conjunta.**](coclass.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **\[ atributo \] appobject** también indica que las funciones y propiedades de [**la coclase**](coclass.md) están disponibles globalmente en la biblioteca de tipos actual.

La representación typeflag para este atributo es TYPEFLAG \_ FAPPOBJECT

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**coclase**](coclass.md)
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

[**Licencia**](licensed.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Versión**](version.md)
</dt> </dl>

 

 