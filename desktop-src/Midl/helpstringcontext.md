---
title: atributo helpstringcontext
description: El atributo \ helpstringcontext \ especifica un identificador de contexto de ayuda de 32 bits en el archivo de ayuda. Puede aplicar el atributo \ helpstringcontext \ a la biblioteca, interfaz, dispinterface, módulo, coclase, instrucciones TypeDef, propiedades, parámetros y métodos.
ms.assetid: 0ac41bd9-ccc6-4b5c-b925-63bff9254eed
keywords:
- helpstringcontext (atributo) MIDL
topic_type:
- apiref
api_name:
- helpstringcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72ddded3beb768543f2f990aa9d656fba1fa8b98
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105651330"
---
# <a name="helpstringcontext-attribute"></a>atributo helpstringcontext

El atributo **\[ helpstringcontext \]** especifica un identificador de contexto de ayuda de 32 bits en el archivo de ayuda. Puede aplicar el atributo **\[ helpstringcontext \]** a la [**biblioteca**](library.md), [**interfaz**](interface.md), [**dispinterface**](dispinterface.md), [**módulo**](module.md), [**coclase**](coclass.md), instrucciones [**typedef**](typedef.md) , propiedades, parámetros y métodos.

``` syntax
[  helpstringcontext(contextid)[, optional-attribute-list]] idl-statement
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*ContextId* 
</dt> <dd>

Entero único que identifica el texto de ayuda asociado a la instrucción MIDL actual.

</dd> <dt>

*opcional-Attribute-List* 
</dt> <dd>

Cero o más atributos de MIDL.

</dd> <dt>

*IDL-Statement* 
</dt> <dd>

La instrucción MIDL a la que se aplicará el atributo **\[ helpstringcontext \]** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use las funciones **GetDocumentation2** en las interfaces **ITypeLib2** e **ITypeInfo2** para recuperar la cadena de ayuda.

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

 

 




