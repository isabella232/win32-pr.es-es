---
title: fault_status atributo)
description: El atributo \ \_ ACF status \ ACF especifica que un código de error de tipo error \_ \_ t indica un error en el procedimiento remoto, en lugar de otros tipos de problemas, como errores de comunicación.
ms.assetid: 9da7bd3d-cef0-4ad4-b2a4-3f8aa156e8e0
keywords:
- fault_status el atributo MIDL
topic_type:
- apiref
api_name:
- fault_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 134d9772e167fe63e133d569b9985a7735668d3c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783611"
---
# <a name="fault_status-attribute"></a>atributo de estado de error \_

El atributo ACF de **\[ \_ estado \]** de error especifica que un código de error de tipo [**error \_ \_ t**](error-status-t.md) indica un error en el procedimiento remoto, en lugar de otros tipos de problemas, como errores de comunicación.

``` syntax
[fault_status [ , ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] parameter-name
    , ... );

[ [ ACF-function-attributes ] ] function-name(
    [fault_status [ , ACF-parameter-attributes ] ] parameter-name
    , ... );
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*ACF: atributos de función* 
</dt> <dd>

Especifica cero o más atributos de función ACF como el **\[ \_ estado \] de error** y **\[** [**nocode**](nocode.md) **\]** . Los atributos de función se incluyen entre corchetes. Tenga en cuenta que cero o más atributos se pueden aplicar a una función. Separe varios atributos de función con comas. Tenga en cuenta también que si el **\[ \_ estado \] de error** aparece como un atributo de función, tampoco puede aparecer como atributo de parámetro.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función tal y como se define en el archivo IDL.

</dd> <dt>

*ACF-Parameter-Attributes* 
</dt> <dd>

Especifica los atributos que se aplican a un parámetro. Tenga en cuenta que se pueden aplicar cero o más atributos al parámetro. Los atributos de parámetro se incluyen entre corchetes. Separe varios atributos de parámetro con comas. Los atributos de parámetros IDL, como los atributos direccionales, no se permiten en ACF. Tenga en cuenta que si el **\[ \_ estado \] de error** aparece como un atributo de parámetro, tampoco puede aparecer como un atributo de función.

</dd> <dt>

*nombre de parámetro* 
</dt> <dd>

Especifica el parámetro para la función tal y como se define en el archivo IDL. Cada parámetro de la función se debe especificar en la misma secuencia, con el mismo nombre que el definido en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo de **\[ \_ estado \] de error** se puede usar como un atributo de función o como un atributo de parámetro, pero solo puede aparecer una vez por función. Se puede aplicar a la propia función o a un parámetro de cada función.

El atributo de **\[ \_ estado \]** de error solo se puede aplicar a funciones que devuelven el tipo de [**Estado de error \_ \_ t**](error-status-t.md). Cuando se produce un error en el procedimiento remoto de forma que hace que se devuelva una PDU de error, se devuelve un código de error.

Cuando el **\[ \_ estado \] de error** se usa como atributo de parámetro, el parámetro debe ser un **\[** [](out-idl.md) **\]** parámetro de salida de tipo [**error de \_ estado \_ t**](error-status-t.md). Si se produce un error de servidor, el parámetro se establece en el código de error. Cuando la llamada remota se completa correctamente, el procedimiento establece el valor.

No es necesario especificar el parámetro asociado al atributo de **\[ \_ estado \] de error** en el archivo IDL. Cuando no se especifica el parámetro, se genera un nuevo parámetro [**out**](out-idl.md) de tipo [**error \_ status \_ t**](error-status-t.md) después del último parámetro definido en el archivo de DCE IDL.

Es posible que los atributos **\[ \_ estado \] de error** y **\[** [**\_ Estado de comunicación**](comm-status.md) **\]** aparezcan en una sola función, ya sea como atributos de función o atributos de parámetro. Si ambos atributos son atributos de función, o si se aplican al mismo parámetro y no se produce ningún error, la función o el parámetro tiene el valor de **Estado de error \_ \_ correcto**. De lo contrario, contiene el valor de código de estado adecuado. Dado que los valores devueltos para el **\[ \_ estado \] de error** son diferentes de los valores devueltos para el **\[ \_ estado \] de COMM**, los valores devueltos se interpretan fácilmente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Estado de COMM \_**](comm-status.md)
</dt> <dt>

[**Estado de error \_ \_ t**](error-status-t.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> </dl>

 

 




