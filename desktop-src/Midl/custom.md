---
title: atributo personalizado
description: El atributo \ custom\ crea un atributo definido por el usuario.
ms.assetid: 63c93eca-c9c1-4c14-9f46-aa78b01d9ff8
keywords:
- MIDL de atributo personalizado
topic_type:
- apiref
api_name:
- custom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace6a558da428da07a432653391e0e48b7a5545bb1a83eb40d9c950abfa9d9aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643674"
---
# <a name="custom-attribute"></a>atributo personalizado

El **\[ atributo \]** personalizado crea un atributo definido por el usuario.

``` syntax
[custom(attribute-id, attribute-value),attribute-list] element-type element-name
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*attribute-id* 
</dt> <dd>

GUID del atributo personalizado.

</dd> <dt>

*attribute-value* 
</dt> <dd>

Valor que contiene el atributo. El valor debe ser uno que se pueda colocar en un tipo VARIANT.

</dd> <dt>

*attribute-list* 
</dt> <dd>

Otros atributos, como **\[** [**uuid**](uuid.md) **\]** y **\[** [**helpstring**](helpstring.md) **\]** , que se aplican a este elemento.

</dd> <dt>

*element-type* 
</dt> <dd>

Tipo de elemento al que se aplica el atributo personalizado. Puede ser una instrucción de biblioteca, información de tipos, una variable, una función o un parámetro. No se puede usar un atributo personalizado en un miembro de una coclase.

</dd> <dt>

*element-name* 
</dt> <dd>

Nombre del elemento.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Use el **\[ atributo \]** personalizado para definir su propio atributo. Por ejemplo, puede crear un atributo con valores de cadena que proporciona el ProgID para una clase.

Para recuperar un valor de atributo personalizado, llame a uno de los siguientes:

-   ITypeLib2::GetCustData(rguid, pvarVal)
-   ITypeInfo2::GetCustData(rguid, pvarVal)
-   ITypeInfo2::GetFuncCustData(index, rguid, pvarVal)
-   ITypeInfo2::GetVarCustData(index, rguid, pvarval)
-   ITypeInfo2::GetParamCustData(indexFunc, indexParam, rguid, pvarVal)

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**Biblioteca**](library.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> </dl>

 

 