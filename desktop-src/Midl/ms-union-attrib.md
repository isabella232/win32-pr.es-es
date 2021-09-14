---
title: ms_union (atributo)
description: La palabra clave \ms union\ se usa para controlar la alineación de API de las uniones \_ nocapsuladas.
ms.assetid: 20ac2985-4552-4224-b03b-07378a2c0cdf
keywords:
- ms_union atributo MIDL
topic_type:
- apiref
api_name:
- ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ad9b750027163aef806f5a66e51f87874a0ad2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159481"
---
# <a name="ms_union-attribute"></a>Atributo \_ de unión ms

La palabra \[ **clave ms \_ union** se usa para controlar la alineación API de las uniones \] nocapsuladas.

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

*interface-name* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*procedure-type* 
</dt> <dd>

Especifica el tipo de valor devuelto del procedimiento al que se aplica el atributo.

</dd> <dt>

*procedure-name* 
</dt> <dd>

Especifica el nombre del procedimiento.

</dd> <dt>

*param-list* 
</dt> <dd>

Especifica la lista de parámetros del procedimiento, que puede estar vacía.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Nunca use este modificador o atributo con nuevas interfaces. Se trata solo de una característica de compatibilidad con versiones anteriores. El compilador MIDL de esta versión de RPC de Microsoft refleja el comportamiento del compilador IDL de DCE de OSF para las uniones no superadas. Sin embargo, dado que las versiones anteriores del compilador MIDL no lo hacían, el modificador de unión [**/ms \_**](-ms-union.md) proporciona compatibilidad con interfaces creadas en versiones anteriores del compilador MIDL.

La **característica de \_ unión ms** se puede usar como un atributo de interfaz IDL, un atributo de tipo IDL o como un modificador de línea de comandos ( [**/ms \_ union**](-ms-union.md)).

## <a name="examples"></a>Ejemplos

``` syntax
[ms_union] long procedure (...);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/ms \_ union**](-ms-union.md)
</dt> </dl>

 

 




