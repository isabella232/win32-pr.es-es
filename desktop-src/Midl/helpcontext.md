---
title: helpcontext (atributo)
description: El atributo \ HelpContext \ especifica un identificador de contexto que permite al usuario ver información sobre este elemento en el archivo de ayuda.
ms.assetid: 44a60c75-be69-4cd9-afb0-5eb988830e6c
keywords:
- atributo ContextoDeAyuda (MIDL)
topic_type:
- apiref
api_name:
- helpcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75a8811a73515528981a8214caba3fe2778e2ea9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995157"
---
# <a name="helpcontext-attribute"></a>helpcontext (atributo)

El \[  \] atributo HelpContext especifica un identificador de contexto que permite al usuario ver información sobre este elemento en el archivo de ayuda.

``` syntax
[
    uuid(uuid-number), 
    helpcontext(helpcontext-value)
    [, attribute-list]
] 
element element-name
{
    definitions
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*UUID-número* 
</dt> <dd>

Especifica un número de identificación único universal para la [**biblioteca**](library.md), \[ [**importlib**](importlib.md) \] , [**interfaz**](interface.md), [**dispinterface**](dispinterface.md), [**módulo**](module.md), [**typedef**](typedef.md), **métodos**, **\[ propiedades \]** o [**coclase**](coclass.md).

</dd> <dt>

*HelpContext: valor* 
</dt> <dd>

Entero único que identifica el texto de ayuda asociado al elemento MIDL actual.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica una lista de uno o más atributos que se aplican al elemento MIDL en conjunto.

</dd> <dt>

*Element* 
</dt> <dd>

Una de las siguientes directivas: [**Library**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Method**, **Property** o [**CoClass**](coclass.md).

</dd> <dt>

*nombre del elemento* 
</dt> <dd>

El nombre que otros componentes de software pueden usar para delimitar el elemento actual.

</dd> <dt>

*Figura* 
</dt> <dd>

Especifica las instrucciones que componen la definición del elemento.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El \[  \] atributo HelpContext se puede aplicar a los elementos siguientes: [**Library**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Method**, **Property** o [**CoClass**](coclass.md).

*HelpContext-Value* es un identificador de contexto de 32 bits dentro del archivo de ayuda que se puede recuperar con las [**funciones GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) en las interfaces [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) y [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) .

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpcontext(7035943),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default, helpcontext(3914972)] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**coclase**](coclass.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**interfaz**](interface.md)
</dt> <dt>

[**biblioteca**](library.md)
</dt> <dt>

[**destina**](module.md)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 