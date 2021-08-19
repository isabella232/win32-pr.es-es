---
title: atributo helpstringcontext
description: El atributo \ helpstringcontext\ especifica un identificador de contexto de Ayuda de 32 bits en el archivo de Ayuda. Puede aplicar el atributo \ helpstringcontext\ a biblioteca, interfaz, dispinterface, módulo, coclass, instrucciones typedef, propiedades, parámetros y métodos.
ms.assetid: 0ac41bd9-ccc6-4b5c-b925-63bff9254eed
keywords:
- Atributo helpstringcontext MIDL
topic_type:
- apiref
api_name:
- helpstringcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64e97ea0d7b41d87ef1d535d562f3b515dda4f59a67f6d5e35f97bed8b1f9ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807240"
---
# <a name="helpstringcontext-attribute"></a>atributo helpstringcontext

El **\[ atributo \] helpstringcontext** especifica un identificador de contexto de Ayuda de 32 bits en el archivo de Ayuda. Puede aplicar el atributo **\[ helpstringcontext \]** a las instrucciones [**library**](library.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**coclass**](coclass.md), [**typedef,**](typedef.md) propiedades, parámetros y métodos.

``` syntax
[  helpstringcontext(contextid)[, optional-attribute-list]] idl-statement
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*contextid* 
</dt> <dd>

Entero único que identifica el texto de ayuda asociado a la instrucción MIDL actual.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Cero o más atributos MIDL.

</dd> <dt>

*idl-statement* 
</dt> <dd>

Instrucción MIDL a la que se aplicará el atributo **\[ helpstringcontext. \]**

</dd> </dl>

## <a name="remarks"></a>Comentarios

Use las **funciones GetDocumentation2** en las interfaces **ITypeLib2** e **ITypeInfo2** para recuperar la cadena de ayuda.

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(. . .),
    helpstringcontext(103),
    version(1.0)
]
library Lines
{
    [
        uuid(. . .), 
        helpstringcontext(102),
        oleautomation,
        dual
    ]
    interface ILine : IDispatch
    {
        [propget, helpstringcontext(100)] HRESULT Color([out, retval] long* ReturnVal); 
        [propput, helpstringcontext(101)] HRESULT Color([in] long rgb);
    }
};
```

 

 




