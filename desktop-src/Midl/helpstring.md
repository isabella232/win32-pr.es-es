---
title: atributo HelpString
description: El atributo \ HelpString \ especifica una cadena de caracteres que se utiliza para describir el elemento al que se aplica.
ms.assetid: f05d3fdd-d975-4f0e-8181-07e16288ff48
keywords:
- atributo HelpString MIDL
topic_type:
- apiref
api_name:
- helpstring
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c58bbe61b10e2f223cf9f662f10d95ca72819b02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995144"
---
# <a name="helpstring-attribute"></a>atributo HelpString

El atributo **\[ HelpString \]** especifica una cadena de caracteres que se utiliza para describir el elemento al que se aplica. Puede aplicar el atributo **\[ HelpString \]** a las instrucciones Library, importlib, interface, dispinterface, Module o coclass, definiciones de tipo, propiedades y métodos.

``` syntax
[
    helpstring(help-text-string)
    [, optional-attribute-list]
] 
element element-name
{
    definition
}

[idl-statement, helpstring(help-text-string)]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Help-Text-String* 
</dt> <dd>

Cadena de caracteres terminada en cero que contiene el texto de ayuda.

</dd> <dt>

*opcional-Attribute-List* 
</dt> <dd>

Cero o más instrucciones de atributo de MIDL.

</dd> <dt>

*Element* 
</dt> <dd>

Una de las siguientes directivas: [**Library**](library.md), **\[** [**importlib**](importlib.md) **\]** , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Method**, **Property** o [**CoClass**](coclass.md).

</dd> <dt>

*nombre del elemento* 
</dt> <dd>

El nombre que otros componentes de software pueden usar para delimitar el elemento actual.

</dd> <dt>

*definición* 
</dt> <dd>

Especifica las instrucciones que componen la definición del elemento.

</dd> <dt>

*IDL-Statement* 
</dt> <dd>

Una instrucción de definición de la interfaz MIDL como [**propget**](propget.md) o [**PROPPUT**](propput.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use las funciones [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) en las interfaces [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) y [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) para recuperar la cadena de ayuda.

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Lines 1.0 Type Library"),
    version(1.0)
]
library Lines
{
     [
         uuid(1e123456-1f3c-1069-996b-00dd010fe676), 
         helpstring("Line object."),
         oleautomation,
         dual
     ]
     interface ILine : IDispatch                         
     {
         [propget, helpstring("Returns and sets RGB color.")]
         HRESULT Color([out, retval] long* ReturnVal); 
         [propput, helpstring("Returns and sets RGB color.")]
         HRESULT Color([in] long rgb);
     }
};
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**biblioteca**](library.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**interfaz**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**destina**](module.md)
</dt> <dt>

[**coclase**](coclass.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 