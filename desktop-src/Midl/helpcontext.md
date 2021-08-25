---
title: helpcontext (atributo)
description: El atributo \ helpcontext\ especifica un identificador de contexto que permite al usuario ver información sobre este elemento en el archivo de Ayuda.
ms.assetid: 44a60c75-be69-4cd9-afb0-5eb988830e6c
keywords:
- atributo helpcontext MIDL
topic_type:
- apiref
api_name:
- helpcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3caa5dd32257fb5d75bbf77cde4ae5e71c6e97574cd1c263ead47aacedccadc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895255"
---
# <a name="helpcontext-attribute"></a>helpcontext (atributo)

El \[ **atributo helpcontext** especifica un identificador de contexto que permite al \] usuario ver información sobre este elemento en el archivo de Ayuda.

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

*uuid-number* 
</dt> <dd>

Especifica un número de identificación único universal para la biblioteca [**,**](library.md) \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **methods**, **\[ property \]** o [**coclass**](coclass.md).

</dd> <dt>

*helpcontext-value* 
</dt> <dd>

Entero único que identifica el texto de ayuda asociado al elemento MIDL actual.

</dd> <dt>

*attribute-list* 
</dt> <dd>

Especifica una lista de uno o varios atributos que se aplican al elemento MIDL en su conjunto.

</dd> <dt>

*Elemento* 
</dt> <dd>

Una de las directivas siguientes: [**library**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property** o [**coclass**](coclass.md).

</dd> <dt>

*element-name* 
</dt> <dd>

Nombre que otros componentes de software pueden usar para delinear el elemento actual.

</dd> <dt>

*Definiciones* 
</dt> <dd>

Especifica las instrucciones que son la definición del elemento.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El atributo helpcontext se puede aplicar a los siguientes \[  \] elementos: [**library**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property** o [**coclass**](coclass.md).

*Helpcontext-value* es un identificador de contexto de 32 bits dentro del archivo de Ayuda que se puede recuperar con las funciones [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) en las interfaces [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) e [**ITypeInfo.**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo)

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

[**Dispinterface**](dispinterface.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**Interfaz**](interface.md)
</dt> <dt>

[**Biblioteca**](library.md)
</dt> <dt>

[**Módulo**](module.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 