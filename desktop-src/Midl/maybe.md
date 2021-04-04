---
title: posible atributo
description: La palabra clave \ maybe \ indica que la llamada a procedimiento remoto no tiene que ejecutarse cada vez que se llama a y el cliente no espera una respuesta. Tenga en cuenta que el protocolo \ tal vez no garantiza la entrega o la finalización de la llamada.
ms.assetid: 163b9fd5-7dce-493e-95bc-63807f42a498
keywords:
- posible atributo MIDL
topic_type:
- apiref
api_name:
- maybe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68704e19d421150444933d74f6b78fc5bada46f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076578"
---
# <a name="maybe-attribute"></a>posible atributo

La palabra clave **\[ puede \]** indicar que la llamada a procedimiento remoto no tiene que ejecutarse cada vez que se llama a y el cliente no espera una respuesta. Tenga en cuenta que el protocolo **\[ maybe \]** no garantiza la entrega ni la finalización de la llamada.

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

Especifica el nombre de la función a la que se aplicará el atributo **\[ maybe \]** .

</dd> <dt>

*params* 
</dt> <dd>

Lista de parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una llamada con el atributo **\[ maybe \]** no puede contener parámetros de salida y es implícitamente una **\[** llamada [**idempotente**](idempotent.md) **\]** .

## <a name="see-also"></a>Vea también

<dl> <dt>

[**amplia**](broadcast.md)
</dt> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




