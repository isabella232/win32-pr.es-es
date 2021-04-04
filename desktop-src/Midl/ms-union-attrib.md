---
title: ms_union (atributo)
description: La palabra clave \ MS \_ Union \ se utiliza para controlar la alineación del NDR de las uniones no encapsuladas.
ms.assetid: 20ac2985-4552-4224-b03b-07378a2c0cdf
keywords:
- ms_union el atributo MIDL
topic_type:
- apiref
api_name:
- ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ad9b750027163aef806f5a66e51f87874a0ad2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076576"
---
# <a name="ms_union-attribute"></a>atributo de unión de MS \_

La palabra clave \[ **MS \_ Union** \] se utiliza para controlar la alineación del NDR de las uniones no encapsuladas.

``` syntax
[
    ms_union,
    ...
]
interface interface-name 
{
    ...
}

[ms_union] procedure-type procedure-name(param-list);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre de interfaz* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*tipo de procedimiento* 
</dt> <dd>

Especifica el tipo de valor devuelto del procedimiento al que se aplica el atributo.

</dd> <dt>

*procedimiento: nombre* 
</dt> <dd>

Especifica el nombre del procedimiento.

</dd> <dt>

*lista de parámetros* 
</dt> <dd>

Especifica la lista de parámetros del procedimiento, que puede estar vacía.

</dd> </dl>

## <a name="remarks"></a>Observaciones

No utilice nunca este modificador o atributo con nuevas interfaces. Esta es solo una característica de compatibilidad con versiones anteriores. El compilador MIDL en esta versión de Microsoft RPC refleja el comportamiento del compilador de OSF DCE IDL para uniones no encapsuladas. Sin embargo, dado que las versiones anteriores del compilador de MIDL no lo hacían, el modificador [**/MS \_ Union**](-ms-union.md) proporciona compatibilidad con las interfaces creadas en versiones anteriores del compilador de MIDL.

La característica **MS \_ Union** se puede usar como un atributo de interfaz IDL, un atributo de tipo IDL o como un modificador de la línea de comandos ( [**/MS \_ Union**](-ms-union.md)).

## <a name="examples"></a>Ejemplos

``` syntax
[ms_union] long procedure (...);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**\_Unión/MS**](-ms-union.md)
</dt> </dl>

 

 




