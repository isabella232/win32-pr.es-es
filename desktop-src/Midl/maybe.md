---
title: atributo maybe
description: La palabra clave \maybe\ indica que la llamada a procedimiento remoto no necesita ejecutarse cada vez que se llama y el cliente no espera una respuesta. Tenga en cuenta que el protocolo \maybe\ no garantiza la entrega ni la finalización de la llamada.
ms.assetid: 163b9fd5-7dce-493e-95bc-63807f42a498
keywords:
- puede que el atributo MIDL
topic_type:
- apiref
api_name:
- maybe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68704e19d421150444933d74f6b78fc5bada46f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159502"
---
# <a name="maybe-attribute"></a>atributo maybe

La palabra **\[ clave puede \]** indicar que la llamada a procedimiento remoto no necesita ejecutarse cada vez que se llama y el cliente no espera una respuesta. Tenga en cuenta **\[ que el protocolo quizás \]** no garantiza la entrega ni la finalización de la llamada.

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

*function-name* 
</dt> <dd>

Especifica el nombre de la función a la que **se \[ \]** aplicará el atributo maybe.

</dd> <dt>

*params* 
</dt> <dd>

Lista de parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una llamada con el **\[ atributo \] maybe** no puede contener parámetros de salida y es implícitamente una llamada **\[** [**idempotente.**](idempotent.md) **\]**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Difusión**](broadcast.md)
</dt> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




