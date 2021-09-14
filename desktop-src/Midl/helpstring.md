---
title: atributo helpstring
description: El atributo \ helpstring\ especifica una cadena de caracteres que se usa para describir el elemento al que se aplica.
ms.assetid: f05d3fdd-d975-4f0e-8181-07e16288ff48
keywords:
- atributo helpstring MIDL
topic_type:
- apiref
api_name:
- helpstring
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c58bbe61b10e2f223cf9f662f10d95ca72819b02
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159561"
---
# <a name="helpstring-attribute"></a>atributo helpstring

El **\[ atributo \] helpstring** especifica una cadena de caracteres que se usa para describir el elemento al que se aplica. Puede aplicar el atributo **\[ helpstring \]** a las instrucciones library, importlib, interface, dispinterface, module o coclass, typedefs, properties y methods.

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

*help-text-string* 
</dt> <dd>

Cadena de caracteres terminada en cero que contiene texto de ayuda.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Cero o más instrucciones de atributo MIDL.

</dd> <dt>

*Elemento* 
</dt> <dd>

Una de las directivas siguientes: [**library**](library.md), **\[** [**importlib**](importlib.md) **\]** , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property** o [**coclass**](coclass.md).

</dd> <dt>

*element-name* 
</dt> <dd>

Nombre que otros componentes de software pueden usar para delinear el elemento actual

</dd> <dt>

*Definición* 
</dt> <dd>

Especifica las instrucciones que son la definición del elemento.

</dd> <dt>

*idl-statement* 
</dt> <dd>

Una instrucción de definición de interfaz MIDL como [**propget**](propget.md) o [**propput**](propput.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use las [**funciones GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) en las interfaces [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) [**e ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) para recuperar la cadena de ayuda.

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

[**Biblioteca**](library.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**Interfaz**](interface.md)
</dt> <dt>

[**Dispinterface**](dispinterface.md)
</dt> <dt>

[**Módulo**](module.md)
</dt> <dt>

[**coclase**](coclass.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 