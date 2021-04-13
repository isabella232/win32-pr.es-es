---
title: appobject (atributo)
description: El atributo \ appobject \ identifica la coclase como un objeto de aplicación, que está asociado a una aplicación EXE completa.
ms.assetid: f4fcdf55-7431-4d66-8a46-f741c52fbe56
keywords:
- appobject (atributo) MIDL
topic_type:
- apiref
api_name:
- appobject
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d937d4a83306bc0c29f3c8c806bc043febec6a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420598"
---
# <a name="appobject-attribute"></a>appobject (atributo)

El atributo **\[ appobject \]** identifica la [**coclase**](coclass.md) como un objeto de aplicación, que está asociado a una aplicación exe completa.

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

*UUID-número* 
</dt> <dd>

Especifica un número de identificación único universal para la [**coclase**](coclass.md).

</dd> <dt>

*coclass-Attribute-List* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la instrucción [**CoClass**](coclass.md) . Los atributos **de coclase** permitidos son [**\[ HelpString \]**](helpstring.md), [**\[ HelpContext \]**](helpcontext.md), con [**\[ licencia \]**](licensed.md), [**\[ versión \]**](version.md), [**\[ control \]**](control.md)y [**\[ oculto \]**](hidden.md).

</dd> <dt>

*classname* 
</dt> <dd>

Especifica el nombre por el que se conoce el objeto de componente en la biblioteca de tipos.

</dd> <dt>

*definición de coclase* 
</dt> <dd>

Especifica las instrucciones que componen la definición de [**coclase**](coclass.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ appobject \]** también indica que las funciones y propiedades de la [**coclase**](coclass.md) están disponibles globalmente en la biblioteca de tipos actual.

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

[**control**](control.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**plusvalía**](hidden.md)
</dt> <dt>

[**bajo**](licensed.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Versión**](version.md)
</dt> </dl>

 

 