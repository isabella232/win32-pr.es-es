---
title: Atributo idempotente
description: El atributo \ idempotent\ especifica que una operación no modifica la información de estado y devuelve los mismos resultados cada vez que se realiza. Realizar la rutina más de una vez tiene el mismo efecto que realizarla una vez.
ms.assetid: 876a40b5-8165-4b5c-bd62-9c43a9eb4b2b
keywords:
- atributo idempotente MIDL
topic_type:
- apiref
api_name:
- idempotent
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82364c6222f6b566ef6aacb5b71a72b49c213f5a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159552"
---
# <a name="idempotent-attribute"></a>Atributo idempotente

El **\[ atributo \] idempotente** especifica que una operación no modifica la información de estado y devuelve los mismos resultados cada vez que se realiza. Realizar la rutina más de una vez tiene el mismo efecto que realizarla una vez.

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

*interface-attribute-list* 
</dt> <dd>

Especifica una lista de cero o más atributos IDL que se aplican a la interfaz en su conjunto. Cuando hay dos o más atributos de interfaz, deben estar separados por comas.

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*attribute-list* 
</dt> <dd>

Especifica atributos adicionales que se aplicarán a la función. Separe varios atributos con comas.

</dd> <dt>

*returntype* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre de la función a la que se aplicará el atributo **\[ \] idempotente.**

</dd> <dt>

*params* 
</dt> <dd>

Lista de parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Observaciones

RPC admite dos tipos de semántica de llamadas remotas: llamadas a operaciones con el atributo **\[ idempotente \]** y llamadas a operaciones (operaciones *idempotentes)* sin el atributo **\[ idempotente \]** (operaciones no *idempotentes).* Una operación idempotente se puede llevar a cabo más de una vez sin ningún efecto negativo. Por el contrario, una operación no idempotente no se puede ejecutar más de una vez porque devolverá resultados diferentes cada vez o porque modifica algún estado.

Para asegurarse de que un procedimiento se vuelva a ejecutar automáticamente si la llamada no se completa, use el **\[ atributo \] idempotente.** Si los **\[ atributos \] idempotentes**, broadcast o maybe no están presentes, el procedimiento usará la semántica no **\[** [](broadcast.md) **\]** **\[** [](maybe.md) **\]** idempotente de forma predeterminada. En este caso, la operación se ejecuta solo una vez.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Difusión**](broadcast.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**quizás**](maybe.md)
</dt> </dl>

 

 




