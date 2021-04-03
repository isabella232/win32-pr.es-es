---
title: comm_status atributo)
description: El atributo \ COMM \_ status \ ACF hace que se devuelva un código de error cuando se produce un error de comunicación durante la ejecución de una función.
ms.assetid: 3ea9ce62-8bd4-40fe-b838-bfebd52b5a15
keywords:
- comm_status el atributo MIDL
topic_type:
- apiref
api_name:
- comm_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4952d03a80dbbffb135043d024b0c0eb18966f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784313"
---
# <a name="comm_status-attribute"></a>atributo de estado de COMM \_

El atributo ACF de **\[ \_ estado \] de COMM** hace que se devuelva un código de error cuando se produce un error de comunicación durante la ejecución de una función.

``` syntax
[comm_status [ , ACF-function-attributes ] ] 
    error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [comm_status [ , ACF-parameter-attributes ] ] error_status_t name
    , ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*ACF: atributos de función* 
</dt> <dd>

Especifica cero o más atributos de función ACF, como el **\[ \_ estado \] de COMM** y **\[** [**nocode**](nocode.md) **\]** . Los atributos de función se incluyen entre corchetes. Cero o más atributos se pueden aplicar a una función. Separe varios atributos de función con comas. Tenga en cuenta que si el **\[ \_ estado \] de COMM** aparece como un atributo de función, tampoco puede aparecer como atributo de parámetro.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función tal y como se define en el archivo IDL.

</dd> <dt>

*ACF-Parameter-Attributes* 
</dt> <dd>

Especifica los atributos que se aplican a un parámetro. Tenga en cuenta que se pueden aplicar cero, uno o varios atributos al parámetro. Separe varios atributos de parámetro con comas. Los atributos de parámetro se incluyen entre corchetes. Los atributos de parámetros IDL, como los atributos direccionales, no se permiten en ACF. Tenga en cuenta que si el **\[ \_ estado \] de COMM** aparece como un atributo de parámetro, tampoco puede aparecer como un atributo de función.

</dd> <dt>

*nombre de parámetro* 
</dt> <dd>

Especifica el parámetro para la función tal y como se define en el archivo IDL. Cada parámetro de la función se debe especificar en la misma secuencia, con el mismo nombre que el definido en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo de **\[ \_ estado \] de COMM** se puede usar como un atributo de función o como un atributo de parámetro, pero solo puede aparecer una vez por función. Se puede aplicar a la función o a un parámetro de cada función.

El atributo de **\[ \_ estado \] de COMM** solo se puede aplicar a funciones que devuelven el tipo de estado de [**error \_ \_ t**](error-status-t.md). Cuando se produce un error de comunicación durante la ejecución de la función, se devuelve un código de error.

Cuando se usa el **\[ \_ estado \] de COMM** como atributo de parámetro, el parámetro debe definirse en el archivo IDL y debe ser un **\[** parámetro [**out**](out-idl.md) **\]** de tipo [**error \_ \_ t**](error-status-t.md). Cuando se produce un error de comunicación durante la ejecución de la función, el parámetro se establece en el código de error. Cuando la llamada remota se completa correctamente, el procedimiento establece el valor.

Es posible que los atributos **\[ \_ estado \] de comunicación** y **\[** [**\_ Estado de error**](fault-status.md) **\]** aparezcan en una sola función, ya sea como atributos de función o atributos de parámetro. Si ambos atributos son atributos de función o si se aplican al mismo parámetro y no se produce ningún error, la función o el parámetro tiene el valor de **Estado de error \_ \_ correcto**. De lo contrario, contiene el valor de estado de **\[ comunicación \_ \]** adecuado o el valor de **\[ \_ estado \] de error** . Dado que los valores devueltos para el **\[ \_ estado \] de COMM** son distintos de los valores devueltos para el **\[ \_ estado \] de error**, los valores devueltos se interpretan fácilmente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Estado de error \_ \_ t**](error-status-t.md)
</dt> <dt>

[**Estado de error \_**](fault-status.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> </dl>

 

 




