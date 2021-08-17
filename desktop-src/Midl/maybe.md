---
title: atributo maybe
description: La palabra clave \maybe\ indica que la llamada a procedimiento remoto no necesita ejecutarse cada vez que se llama a y el cliente no espera una respuesta. Tenga en cuenta que el protocolo \maybe\ no garantiza la entrega ni la finalización de la llamada.
ms.assetid: 163b9fd5-7dce-493e-95bc-63807f42a498
keywords:
- quizás atributo MIDL
topic_type:
- apiref
api_name:
- maybe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 178faf3d308f7dd282e31a8f0eabf8708bb8b3fe1a0d52a981e65adddb258ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067155"
---
# <a name="maybe-attribute"></a>atributo maybe

La palabra **\[ clave puede \]** indicar que la llamada a procedimiento remoto no necesita ejecutarse cada vez que se llama a y el cliente no espera una respuesta. Tenga en cuenta **\[ que el protocolo quizás \]** no garantiza la entrega ni la finalización de la llamada.

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [maybe [, attribute-list]] returntype function-name(params)
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

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función a la que **\[ \] se** aplicará el atributo maybe.

</dd> <dt>

*params* 
</dt> <dd>

Lista de parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una llamada con el **\[ atributo \] maybe** no puede contener parámetros de salida y es implícitamente una llamada **\[** [**idempotente.**](idempotent.md) **\]**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Difusión**](broadcast.md)
</dt> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




