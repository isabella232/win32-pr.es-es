---
title: fault_status atributo
description: El atributo \ fault status\ ACF especifica que un código de error de tipo estado de error t indica un error del procedimiento remoto, en lugar de otros tipos de problemas, como errores \_ \_ de \_ comunicación.
ms.assetid: 9da7bd3d-cef0-4ad4-b2a4-3f8aa156e8e0
keywords:
- fault_status atributo MIDL
topic_type:
- apiref
api_name:
- fault_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 134d9772e167fe63e133d569b9985a7735668d3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159591"
---
# <a name="fault_status-attribute"></a>atributo \_ de estado de error

El **\[ atributo \_ \]** ACF de estado de error especifica que un código de error de tipo estado de [**error \_ \_ t**](error-status-t.md) indica un error del procedimiento remoto, en lugar de otros tipos de problemas, como errores de comunicación.

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

*Atributos de función de ACF* 
</dt> <dd>

Especifica cero o más atributos de función de ACF, como **\[ el estado de error \_ y \]** **\[** [**la codificación**](nocode.md) **\]** . Los atributos de función se incluyen entre corchetes. Tenga en cuenta que se pueden aplicar cero o más atributos a una función. Separe varios atributos de función con comas. Tenga en cuenta también que **\[ si el estado del \_ error \]** aparece como un atributo de función, tampoco puede aparecer como un atributo de parámetro.

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre de la función tal como se define en el archivo IDL.

</dd> <dt>

*ACF-parameter-attributes* 
</dt> <dd>

Especifica los atributos que se aplican a un parámetro. Tenga en cuenta que se pueden aplicar cero o más atributos al parámetro . Los atributos de parámetro se incluyen entre corchetes. Separe varios atributos de parámetro con comas. Los atributos de parámetro IDL, como los atributos direccionales, no se permiten en el ACF. Tenga en cuenta **\[ que si el estado \_ del \]** error aparece como un atributo de parámetro, no puede aparecer también como un atributo de función.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Especifica el parámetro para la función tal como se define en el archivo IDL. Cada parámetro de la función debe especificarse en la misma secuencia, con el mismo nombre definido en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ atributo de \_ estado \]** de error se puede usar como atributo de función o como atributo de parámetro, pero solo puede aparecer una vez por función. Se puede aplicar a la propia función o a un parámetro de cada función.

El **\[ atributo de \_ estado \]** de error solo se puede aplicar a las funciones que devuelven el tipo [**de estado de error \_ \_ t**](error-status-t.md). Cuando se produce un error en el procedimiento remoto de una manera que hace que se devuelva una PDU de error, se devuelve un código de error.

Cuando **\[ se usa \_ el \]** estado de error como atributo de parámetro, el parámetro debe ser un **\[** [**parámetro out**](out-idl.md) de tipo **\]** estado de error [**\_ \_ t**](error-status-t.md). Si se produce un error de servidor, el parámetro se establece en el código de error. Cuando la llamada remota se completa correctamente, el procedimiento establece el valor .

El parámetro asociado al **\[ atributo de \_ estado \]** de error no tiene que especificarse en el archivo IDL. Cuando no se especifica el parámetro , se genera un nuevo parámetro [**out**](out-idl.md) de tipo estado [**de error \_ \_ t**](error-status-t.md) después del último parámetro definido en el archivo IDL de DCE.

Es posible que los atributos de estado **\[ \_ \]** de error y de estado de comm aparezcan en una sola función, ya sea como atributos de función o atributos **\[** [**\_**](comm-status.md) de **\]** parámetro. Si ambos atributos son atributos de función o si se aplican al mismo parámetro y no se produce ningún error, la función o el parámetro tienen el estado de error de valor **\_ \_ correcto.** De lo contrario, contiene el valor de código de estado adecuado. Dado que los valores devueltos **\[ para el estado \_ de \]** error son diferentes de los valores devueltos para el estado de **\[ comm \_ \]**, los valores devueltos se interpretan fácilmente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**estado de \_ comm**](comm-status.md)
</dt> <dt>

[**error \_ status \_ t**](error-status-t.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> </dl>

 

 




