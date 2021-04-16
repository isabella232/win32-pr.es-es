---
title: atributo personalizado
description: El atributo \ custom \ crea un atributo definido por el usuario.
ms.assetid: 63c93eca-c9c1-4c14-9f46-aa78b01d9ff8
keywords:
- atributo personalizado MIDL
topic_type:
- apiref
api_name:
- custom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7c4210091cc028d7724cb40724f22a91eb7d74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105685690"
---
# <a name="custom-attribute"></a>atributo personalizado

El atributo **\[ personalizado \]** crea un atributo definido por el usuario.

``` syntax
[custom(attribute-id, attribute-value),attribute-list] element-type element-name
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador de atributo* 
</dt> <dd>

GUID del atributo personalizado.

</dd> <dt>

*atributo-valor* 
</dt> <dd>

Valor que contiene el atributo. El valor debe ser uno que se pueda colocar en un tipo VARIANT.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Otros atributos, como **\[** [**UUID**](uuid.md) **\]** y **\[** [**HelpString**](helpstring.md) **\]** , que se aplican a este elemento.

</dd> <dt>

*tipo de elemento* 
</dt> <dd>

El tipo de elemento al que se aplica el atributo personalizado. Puede ser una instrucción de biblioteca, información de tipos, una variable, una función o un parámetro. No se puede usar un atributo personalizado en un miembro de una coclase.

</dd> <dt>

*nombre del elemento* 
</dt> <dd>

Nombre del elemento.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use el atributo **\[ personalizado \]** para definir su propio atributo. Por ejemplo, puede crear un atributo con valores de cadena que proporcione el ProgID para una clase.

Para recuperar un valor de atributo personalizado, llame a uno de los siguientes:

-   ITypeLib2:: GetCustData (rguid, pvarVal)
-   ITypeInfo2:: GetCustData (rguid, pvarVal)
-   ITypeInfo2:: GetFuncCustData (índice, rguid, pvarVal)
-   ITypeInfo2:: GetVarCustData (índice, rguid, pvarval)
-   ITypeInfo2:: GetParamCustData (indexFunc, indexParam, rguid, pvarVal)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**biblioteca**](library.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**uuid**](uuid.md)
</dt> </dl>

 

 