---
title: idempotente (atributo)
description: El atributo \ idempotente \ especifica que una operación no modifica información de estado y devuelve los mismos resultados cada vez que se realiza. Realizar la rutina más de una vez tiene el mismo efecto que realizarla una vez.
ms.assetid: 876a40b5-8165-4b5c-bd62-9c43a9eb4b2b
keywords:
- atributo idempotente (MIDL)
topic_type:
- apiref
api_name:
- idempotent
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82364c6222f6b566ef6aacb5b71a72b49c213f5a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104532602"
---
# <a name="idempotent-attribute"></a>idempotente (atributo)

El atributo **\[ idempotente \]** especifica que una operación no modifica la información de estado y devuelve los mismos resultados cada vez que se realiza. Realizar la rutina más de una vez tiene el mismo efecto que realizarla una vez.

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [idempotent [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*interfaz-atributo-lista* 
</dt> <dd>

Especifica una lista de cero o más atributos IDL que se aplican a la interfaz en conjunto. Cuando dos o más atributos de interfaz están presentes, deben separarse con comas.

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica los atributos adicionales que se van a aplicar a la función. Separe varios atributos con comas.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función a la que se aplicará el atributo **\[ idempotente \]** .

</dd> <dt>

*params* 
</dt> <dd>

Lista de parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Observaciones

RPC admite dos tipos de semántica de llamadas remotas: llama a las operaciones con el atributo **\[ idempotente \]** y llama a las operaciones (operaciones *idempotente* ) sin el atributo **\[ idempotente \]** (operaciones *no idempotente* ). Una operación idempotente se puede llevar a cabo más de una vez sin ningún efecto. Por el contrario, una operación no idempotente no se puede ejecutar más de una vez, ya que devolverá resultados diferentes cada vez o porque modificará algún Estado.

Para asegurarse de que un procedimiento se vuelve a ejecutar automáticamente si la llamada no se completa, utilice el atributo **\[ idempotente \]** . Si los atributos **\[ idempotente \]**, **\[** [**Broadcast**](broadcast.md) **\]** o **\[** [**maybe**](maybe.md) **\]** no están presentes, el procedimiento usará la semántica no idempotente de forma predeterminada. En este caso, la operación se ejecuta solo una vez.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**amplia**](broadcast.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**incluso**](maybe.md)
</dt> </dl>

 

 




