---
title: hidden (atributo)
description: El atributo \ Hidden \ indica que el elemento existe pero no debe mostrarse en un explorador orientado al usuario.
ms.assetid: bf1f9270-fb93-4421-804e-d56e2c863bbd
keywords:
- MIDL de atributo oculto
topic_type:
- apiref
api_name:
- hidden
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1718351ef84199b60ba720ed2f3569cfa78a0a50
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651356"
---
# <a name="hidden-attribute"></a>hidden (atributo)

El atributo **\[ Hidden \]** indica que el elemento existe pero no debe mostrarse en un explorador orientado al usuario.

``` syntax
[
    other-attributes, 
    hidden
] 
element element-name
{
    definitions
}

[other-attributes, hidden] function-type function-name(optional-parameter-list);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*otros: atributos* 
</dt> <dd>

Cero o más atributos de MIDL opcionales.

</dd> <dt>

*Element* 
</dt> <dd>

Una de las siguientes directivas: [**CoClass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md)o [**Library**](library.md).

</dd> <dt>

*nombre del elemento* 
</dt> <dd>

El nombre que otros componentes de software pueden usar para delimitar el elemento actual.

</dd> <dt>

*Figura* 
</dt> <dd>

Especifica las instrucciones que componen la definición del elemento.

</dd> <dt>

*tipo de función* 
</dt> <dd>

Tipo de valor devuelto de la función.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Nombre que se usa para invocar la función.

</dd> <dt>

*opcional-parameter-list* 
</dt> <dd>

Cero o más parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ Hidden \]** permite quitar miembros de la interfaz (mediante la protección del uso adicional) y mantener la compatibilidad con el código existente. Puede usar el atributo **\[ Hidden \]** en las propiedades, los métodos y las instrucciones [**CoClass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md)y [**Library**](library.md) .

Cuando se especifica para una biblioteca, el atributo **\[ Hidden \]** evita que se muestre toda la biblioteca. Este uso está diseñado para emplearlo con controles. Los hosts deben crear una biblioteca de tipos que ajuste el control con propiedades extendidas.

### <a name="flags"></a>Marcas

VARFLAG \_ FHIDDEN, FUNCFLAG \_ FHIDDEN, TYPEFLAG \_ FHIDDEN

## <a name="examples"></a>Ejemplos

``` syntax
[hidden, vararg] SAFEARRAY (int) SecretFunc(
    [in, out] SAFEARRAY (variant) *varP) ;

[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    hidden, 
    version (3.0)
] 
library HiddenLib 
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**coclase**](coclass.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**interfaz**](interface.md)
</dt> <dt>

[**biblioteca**](library.md)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> </dl>

 

 