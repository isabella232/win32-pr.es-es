---
title: hidden (atributo)
description: El atributo \ hidden\ indica que el elemento existe, pero no debe mostrarse en un explorador orientado al usuario.
ms.assetid: bf1f9270-fb93-4421-804e-d56e2c863bbd
keywords:
- atributo oculto MIDL
topic_type:
- apiref
api_name:
- hidden
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1718351ef84199b60ba720ed2f3569cfa78a0a50
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159557"
---
# <a name="hidden-attribute"></a>hidden (atributo)

El **\[ atributo \]** oculto indica que el elemento existe, pero no debe mostrarse en un explorador orientado al usuario.

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

*otros atributos* 
</dt> <dd>

Cero o más atributos MIDL opcionales.

</dd> <dt>

*Elemento* 
</dt> <dd>

Una de las directivas siguientes: [**coclase**](coclass.md), [**dispinterface,**](dispinterface.md) [**interfaz**](interface.md)o [**biblioteca**](library.md).

</dd> <dt>

*element-name* 
</dt> <dd>

Nombre que otros componentes de software pueden usar para delinear el elemento actual.

</dd> <dt>

*Definiciones* 
</dt> <dd>

Especifica las instrucciones que son la definición del elemento.

</dd> <dt>

*function-type* 
</dt> <dd>

Tipo de valor devuelto de la función.

</dd> <dt>

*function-name* 
</dt> <dd>

Nombre utilizado para invocar la función.

</dd> <dt>

*optional-parameter-list* 
</dt> <dd>

Cero o más parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ atributo \]** oculto permite quitar miembros de la interfaz (al protegerlos para que no se usen más) al tiempo que se mantiene la compatibilidad con el código existente. Puede usar el atributo **\[ oculto en \] propiedades,** métodos y las instrucciones de biblioteca , [**dispinterface**](dispinterface.md), [**interface**](interface.md)y [**de**](library.md) la [**coclase**](coclass.md).

Cuando se especifica para una biblioteca, el **\[ atributo oculto \]** impide que se muestre toda la biblioteca. Este uso está diseñado para emplearlo con controles. Los hosts deben crear una biblioteca de tipos que ajuste el control con propiedades extendidas.

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

[**Dispinterface**](dispinterface.md)
</dt> <dt>

[**coclase**](coclass.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Interfaz**](interface.md)
</dt> <dt>

[**Biblioteca**](library.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> </dl>

 

 