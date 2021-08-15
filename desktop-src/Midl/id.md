---
title: Atributo id
description: El atributo \ id\ especifica un DISPID para una función miembro (ya sea una propiedad o un método, en una interfaz o dispinterface).
ms.assetid: 6f1be049-81b4-4aa2-a893-5dd79bb4d63c
keywords:
- atributo id MIDL
topic_type:
- apiref
api_name:
- id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a4d783265ebfcf9dca454c80c39031dc0c37dfb63a8749b4d0e6299a510d91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643071"
---
# <a name="id-attribute"></a>Atributo id

El **\[ atributo id \]** especifica un DISPID para una función miembro (ya sea una propiedad o un método, en una interfaz o dispinterface).

``` syntax
[id(id-num) [,optional-attribute-list]] return-type function-name(optional-parameter-list)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*id-num* 
</dt> <dd>

DISPID para la función.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Especifica una lista de cero o más atributos de interfaz MIDL.

</dd> <dt>

*return-type* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función en el archivo IDL.

</dd> <dt>

*optional-parameter-list* 
</dt> <dd>

Cero o más parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use el atributo **\[ id \]** cuando desee asignar un DISPID estándar (como DISPID VALUE, DISPID NEWENUM, etc.) a un método o propiedad, o cuando implemente su propio \_ \_ **IDispatch::Invoke** en lugar de delegar a **DispInvoke** / **ITypeInfo::Invoke**.

Si no usa el atributo **\[ id \]** en una interfaz, el compilador MIDL le asignará un DISPID. Sin embargo, cuando se especifica una interfaz dispinterface mediante propiedades y métodos, debe especificar un DISPID para cada propiedad y método.

*Id-num es* un valor entero positivo de 32 bits. Los ID negativos están reservados para que los use Automation.

## <a name="examples"></a>Ejemplos

``` syntax
interface IKnown : IUnknown
{
    properties:
        [id(90), propget, 
         helpstring("A meaningful comment."] long Func1(void);

    /* Other interface statements */
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz**](interface.md)
</dt> <dt>

[**Dispinterface**](dispinterface.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 