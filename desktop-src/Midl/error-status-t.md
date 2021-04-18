---
title: error_status_t atributo)
description: La \_ \_ palabra clave de estado de error t designa un tipo para un objeto que contiene información sobre el estado de la comunicación o el estado de error.
ms.assetid: 7eff0d20-c058-4f16-a3db-0b4c82303135
keywords:
- error_status_t el atributo MIDL
topic_type:
- apiref
api_name:
- error_status_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d017b4eaf460b5d5b7ecb8a0bd79201ac8bdee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104357999"
---
# <a name="error_status_t-attribute"></a>atributo de estado de error \_ \_ t

La palabra clave de **Estado de error \_ \_ t** designa un tipo para un objeto que contiene información sobre el estado de la comunicación o el estado de error.

``` syntax
[ [ , ACF-function-attributes ] ] error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] error_status_t parameter-name
    , ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*ACF: atributos de función* 
</dt> <dd>

Especifica cero o más atributos de función ACF, como el **\[** [**\_ Estado de COMM**](comm-status.md) **\]** , el **\[** [**\_ Estado de error**](fault-status.md) **\]** o **\[** [**nocode**](nocode.md) **\]** . Los atributos de función se incluyen entre corchetes. Cero o más atributos se pueden aplicar a una función. Separe varios atributos de función con comas.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función tal y como se define en el archivo IDL.

</dd> <dt>

*ACF-Parameter-Attributes* 
</dt> <dd>

Especifica los atributos que se aplican a un parámetro. Tenga en cuenta que se pueden aplicar cero, uno o varios atributos al parámetro. Separe varios atributos de parámetro con comas. Los atributos de parámetro se incluyen entre corchetes. Los atributos de parámetros IDL, como los atributos direccionales, no se permiten en ACF.

</dd> <dt>

*nombre de parámetro* 
</dt> <dd>

Especifica el parámetro para la función tal y como se define en el archivo IDL. Cada parámetro de la función se debe especificar en la misma secuencia, con el mismo nombre que el definido en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El tipo de **Estado de error \_ \_ t** se usa como parte de la arquitectura de control de excepciones en IDL. Este tipo se asigna a una [**longitud**](long.md) [**sin signo**](unsigned.md) . Las aplicaciones que detectan situaciones de error tienen un **\[** [](out-idl.md) **\]** parámetro de salida o un tipo de valor devuelto de un procedimiento especificado como **Estado de error \_ \_ t**, y califican el **Estado de error \_ \_ t** con los **\[** atributos de estado de la [**comunicación \_**](comm-status.md) **\]** o **\[** [**\_ Estado**](fault-status.md) **\]** de error de ACF. Si el parámetro o el tipo de valor devuelto no se calificó con los atributos de estado de **\[ comunicación \_ \]** o **\[ \_ estado \] de error** , el parámetro funciona como si fuera una longitud sin signo.

A partir de la versión 2,0, el compilador MIDL genera código auxiliar que contiene la arquitectura de control de errores adecuada. Sin embargo, las versiones anteriores del compilador de MIDL administraban un parámetro o tipo de valor devuelto de **Estado de error \_ \_ t** como si se aplicaran los atributos de estado de **\[** [**comunicación \_**](comm-status.md) **\]** y **\[** [**\_ Estado**](fault-status.md) de error **\]** , aunque no fueran. Con MIDL 2,0 o posterior, debe aplicar explícitamente los atributos de estado de **\[ comunicación \_ \]** y **\[ \_ estado \] de error** al parámetro o al procedimiento de ACF.

El tipo de **Estado de error \_ \_ t** es uno de los tipos predefinidos del lenguaje de definición de interfaz. Los tipos predefinidos pueden aparecer como especificadores de tipo en las declaraciones [**typedef**](typedef.md) , en las declaraciones generales y en los declaradores de función (como los especificadores de tipo de valor de función o tipo de parámetro).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estado de COMM \_**](comm-status.md)
</dt> <dt>

[**Estado de error \_**](fault-status.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**tal**](long.md)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**sin signo**](unsigned.md)
</dt> </dl>

 

 




