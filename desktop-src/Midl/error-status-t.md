---
title: error_status_t atributo
description: La palabra clave t de estado de error \_ \_ designa un tipo para un objeto que contiene información sobre el estado de la comunicación o el estado de error.
ms.assetid: 7eff0d20-c058-4f16-a3db-0b4c82303135
keywords:
- error_status_t atributo MIDL
topic_type:
- apiref
api_name:
- error_status_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d017b4eaf460b5d5b7ecb8a0bd79201ac8bdee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159593"
---
# <a name="error_status_t-attribute"></a>error \_ status \_ t attribute

La **palabra clave \_ \_ t** de estado de error designa un tipo para un objeto que contiene información sobre el estado de la comunicación o el estado de error.

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

*ACF-function-attributes* 
</dt> <dd>

Especifica cero o más atributos de función ACF, como **\[** [**el estado de la \_**](comm-status.md) **\]** notificación, el estado **\[** [**\_ de**](fault-status.md) **\]** error o el código **\[** [**nocode**](nocode.md) **\]** . Los atributos de función se incluyen entre corchetes. Se pueden aplicar cero o más atributos a una función. Separe varios atributos de función con comas.

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre de la función tal como se define en el archivo IDL.

</dd> <dt>

*ACF-parameter-attributes* 
</dt> <dd>

Especifica los atributos que se aplican a un parámetro. Tenga en cuenta que se pueden aplicar cero, uno o más atributos al parámetro . Separe varios atributos de parámetro con comas. Los atributos de parámetro se incluyen entre corchetes. Los atributos de parámetro IDL, como los atributos direccionales, no se permiten en el ACF.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Especifica el parámetro para la función tal como se define en el archivo IDL. Cada parámetro de la función debe especificarse en la misma secuencia, con el mismo nombre definido en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **tipo t de \_ \_ estado** de error se usa como parte de la arquitectura de control de excepciones en IDL. Este tipo se asigna a [**un largo sin signo.**](unsigned.md) [](long.md) Las aplicaciones que detectan situaciones de error tienen un parámetro out o un tipo de valor devuelto de un procedimiento especificado como estado de error t y califican el estado de error t con los atributos de estado de error o de correo electrónico en **\[** [](out-idl.md) **\]** el **\_ \_** **\_ \_** **\[** [**\_**](comm-status.md) **\]** **\[** [**\_**](fault-status.md) **\]** ACF. Si el parámetro o el tipo de valor devuelto no se han calificado con los atributos de estado de **\[ comm \_ \]** **\[ \_ \]** o de estado de error, el parámetro funciona como si fuera un long sin signo.

A partir de la versión 2.0, el compilador de MIDL genera código auxiliar que contiene la arquitectura de control de errores adecuada. Sin embargo, las versiones anteriores del compilador MIDL administraban un parámetro o tipo de valor devuelto de estado de **error \_ \_ t** como si se aplicara el estado de comm y los atributos de estado de error, aunque no lo **\[** [**\_**](comm-status.md) **\]** **\[** [**\_**](fault-status.md) **\]** estuvieran. Con MIDL 2.0 o posterior, debe aplicar explícitamente los atributos de estado de **\[ comm \_ \]** **\[ \_ \]** y de estado de error al parámetro o procedimiento en el ACF.

El **tipo t de \_ \_ estado** de error es uno de los tipos predefinidos del lenguaje de definición de interfaz. Los tipos predefinidos pueden aparecer como especificadores de tipo en declaraciones [**typedef,**](typedef.md) en declaraciones generales y en declaradores de función (como function-return-type o como especificadores de tipo de parámetro).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**estado de \_ comm**](comm-status.md)
</dt> <dt>

[**estado \_ de error**](fault-status.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Largo**](long.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> </dl>

 

 




