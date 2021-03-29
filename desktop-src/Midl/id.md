---
title: Atributo id
description: El atributo \ ID \ especifica un DISPID para una función miembro (ya sea una propiedad o un método, en una interfaz o dispinterface).
ms.assetid: 6f1be049-81b4-4aa2-a893-5dd79bb4d63c
keywords:
- identificador del atributo MIDL
topic_type:
- apiref
api_name:
- id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c57d8ea818bbd7b8fd5bd35816e6b7227eb917
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420572"
---
# <a name="id-attribute"></a>Atributo id

El atributo **\[ ID \]** especifica un DISPID para una función miembro (ya sea una propiedad o un método, en una interfaz o dispinterface).

``` syntax
[id(id-num) [,optional-attribute-list]] return-type function-name(optional-parameter-list)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador: número* 
</dt> <dd>

DISPID para la función.

</dd> <dt>

*opcional-Attribute-List* 
</dt> <dd>

Especifica una lista de cero o más atributos de la interfaz de MIDL.

</dd> <dt>

*tipo de valor devuelto* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función en el archivo IDL.

</dd> <dt>

*opcional-parameter-list* 
</dt> <dd>

Cero o más parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Utilice el atributo **\[ \] ID** cuando desee asignar un DISPID estándar (como el \_ valor de DISPID, el DISPID NEWENUM, \_ etc.) a un método o propiedad, o al implementar su propio **IDispatch:: Invoke** en lugar de delegar en **DispInvoke** / **ITypeInfo:: Invoke**.

Si no utiliza el atributo **\[ ID \]** en una interfaz, el compilador MIDL le asignará un DispId. Sin embargo, cuando se especifica una dispinterface mediante propiedades y métodos, se debe especificar un DISPID para cada propiedad y método.

El *identificador-NUM* es un valor entero positivo de 32 bits. Los identificadores negativos se reservan para su uso con la automatización.

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

[**interfaz**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 