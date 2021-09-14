---
title: comm_status atributo
description: El atributo \ comm status\ ACF hace que se devuelva un código de error cuando se produce un error de comunicación durante la \_ ejecución de una función.
ms.assetid: 3ea9ce62-8bd4-40fe-b838-bfebd52b5a15
keywords:
- comm_status atributo MIDL
topic_type:
- apiref
api_name:
- comm_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4952d03a80dbbffb135043d024b0c0eb18966f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159648"
---
# <a name="comm_status-attribute"></a>Atributo de \_ estado de comm

El atributo ACF **\[ \_ de \]** estado de comunicación hace que se devuelva un código de error cuando se produce un error de comunicación durante la ejecución de una función.

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

*Atributos de función de ACF* 
</dt> <dd>

Especifica cero o más atributos de función de ACF, como **\[ el estado de comm \_ \]** y **\[** [**nocode**](nocode.md) **\]** . Los atributos de función se incluyen entre corchetes. Se pueden aplicar cero o más atributos a una función. Separe varios atributos de función con comas. Tenga en cuenta que **\[ si el estado de \_ comm \]** aparece como un atributo de función, no puede aparecer también como un atributo de parámetro.

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre de la función tal como se define en el archivo IDL.

</dd> <dt>

*ACF-parameter-attributes* 
</dt> <dd>

Especifica los atributos que se aplican a un parámetro. Tenga en cuenta que se pueden aplicar cero, uno o más atributos al parámetro . Separe varios atributos de parámetro con comas. Los atributos de parámetro se incluyen entre corchetes. Los atributos de parámetro IDL, como los atributos direccionales, no se permiten en el ACF. Tenga en cuenta que **\[ si el estado de \_ comm \]** aparece como un atributo de parámetro, no puede aparecer también como un atributo de función.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Especifica el parámetro para la función tal como se define en el archivo IDL. Cada parámetro de la función debe especificarse en la misma secuencia, con el mismo nombre definido en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ atributo de estado \_ de \] comm** se puede usar como atributo de función o como atributo de parámetro, pero solo puede aparecer una vez por función. Se puede aplicar a la función o a un parámetro de cada función.

El **\[ atributo de estado \_ de \] comm** solo se puede aplicar a funciones que devuelven el estado [**de error de tipo \_ \_ t**](error-status-t.md). Cuando se produce un error de comunicación durante la ejecución de la función, se devuelve un código de error.

Cuando se usa **\[ \_ el \]** estado de comm como atributo de **\[** [](out-idl.md) **\]** [**\_ \_ parámetro,**](error-status-t.md)el parámetro debe definirse en el archivo IDL y debe ser un parámetro out de tipo estado de error t . Cuando se produce un error de comunicación durante la ejecución de la función, el parámetro se establece en el código de error. Cuando la llamada remota se completa correctamente, el procedimiento establece el valor .

Es posible que los atributos de estado de **\[ \_ \] comm** y de estado de error aparezcan en una sola función, ya sea como atributos de función o atributos **\[** [**\_**](fault-status.md) **\]** de parámetro. Si ambos atributos son atributos de función o si se aplican al mismo parámetro y no se produce ningún error, la función o el parámetro tienen el estado de error de valor **\_ \_ correcto.** De lo contrario, contiene el estado de la página **\[ \_ correspondiente o \]** el valor de estado **\[ \_ de \]** error. Dado que los valores devueltos para el estado **\[ de comm \_ \]** son diferentes **\[ \_ \]** de los valores devueltos para el estado de error , los valores devueltos se interpretan fácilmente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**error \_ status \_ t**](error-status-t.md)
</dt> <dt>

[**estado \_ de error**](fault-status.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> </dl>

 

 




