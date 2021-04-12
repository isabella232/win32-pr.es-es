---
title: atributo de canalización
description: El constructor de tipo de canalización permite transmitir un flujo abierto de datos con tipo a través de una llamada a procedimiento remoto.
ms.assetid: 85b76a55-8df2-4417-9a39-3e3bf49651fc
keywords:
- atributo de canalización MIDL
topic_type:
- apiref
api_name:
- pipe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0aaab8d399c99e02b5393ee9f5258da53aea491
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358849"
---
# <a name="pipe-attribute"></a>atributo de canalización

El constructor de tipo de **canalización** permite transmitir un flujo abierto de datos con tipo a través de una llamada a procedimiento remoto.

``` syntax
typedef pipe element-type pipe-declarator;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo de elemento* 
</dt> <dd>

Define el tamaño de un único elemento en el búfer de transferencia. El tipo *de elemento* puede ser un [tipo base](midl-base-types.md), un tipo predefinido \_ , un [**struct**](struct.md), una [**enumeración 32B**](v1-enum.md)o un identificador de tipo. Se aplican varias restricciones a los *\_ tipos de elemento*, como se describe en la sección Comentarios a continuación.

</dd> <dt>

*declarador de canalización* 
</dt> <dd>

Especifica uno o más identificadores o punteros a los identificadores. Separe varios declaradores con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede usar el constructor de tipo de **canalización** para transmitir datos en ambas direcciones. Un **\[** [](in.md) **\]** parámetro in Pipe permite al servidor extraer el flujo de datos del cliente durante una llamada a procedimiento remoto. Un **\[** parámetro [**out**](out-idl.md) **\]** Pipe permite que el servidor devuelva la secuencia de datos al cliente. Proporcione las rutinas del lado cliente para insertar y extraer el flujo de datos y para asignar un búfer global para los datos. Las rutinas de código auxiliar de cliente y servidor calculan las referencias de los datos y no las calculan y pasan una referencia al búfer de nuevo a la aplicación.

Las restricciones siguientes se aplican a las canalizaciones:

-   Un elemento de canalización no puede ser o contener un puntero, una matriz ajustada o variable, un identificador o un identificador de contexto. Además, en la implementación de canalizaciones de Microsoft, un elemento de canalización no puede ser ni contener una [**Unión**](union.md), una [**enumeración de 16B**](enum.md)o una [**\_ \_ int3264**](--int3264.md).
-   No se pueden aplicar los **\[** atributos [**transmitir \_ como**](transmit-as.md) **\]** , **\[** [**representar \_ como**](represent-as.md) **\]** , **\[** [**\_ serialización de conexión**](wire-marshal.md) **\]** o cálculo de **\[** [**\_ referencias de usuario**](user-marshal.md) **\]** a un tipo de canalización o a un tipo *de elemento*.
-   Un tipo de canalización no puede ser un miembro de una estructura o Unión, el destino de un puntero o el tipo base de una matriz.
-   Un tipo de datos declarado como un tipo de canalización solo se puede usar como parámetro de una llamada remota.
-   Puede pasar un parámetro de canalización en cualquier dirección por valor o por referencia (puntero de referencia **\[** [](ref.md) **\]** ). Sin embargo, no se puede aplicar el **\[** [](ptr.md) **\]** atributo PTR a una canalización que se pasa por referencia. No se puede especificar un parámetro de canalización con un **\[** puntero [**único**](unique.md) **\]** o completo, independientemente de la dirección.
-   No se pueden usar canalizaciones en interfaces de **\[** [**objeto**](object.md) **\]** .
-   No se puede aplicar el **\[** [](idempotent.md) **\]** atributo idempotente a una rutina que tenga un parámetro de canalización.
-   No puede usar los atributos de serialización, **\[** [**codificar**](encode.md) **\]** y **\[** [**descodificar**](decode.md) **\]** con canalizaciones.
-   No se pueden usar identificadores automáticos, de forma predeterminada, ni con el atributo de **\[** [**\_ control automático**](auto-handle.md) **\]** , con canalizaciones.

> [!Note]  
> El compilador MIDL solo admite canalizaciones en modo [**/OIF**](-oi.md) .

 

Para obtener más información sobre cómo implementar rutinas con parámetros de canalización, vea [canalizaciones](/windows/desktop/Rpc/pipes) en la guía y referencia del programador de RPC.

## <a name="examples"></a>Ejemplos

``` syntax
typedef pipe unsigned char UCHAR_PIPE1, UCHAR_PIPE2;
 
//SIMPLE_STRUCT defined elsewhere
typedef pipe SIMPLE_STRUCT SIMPLE_STRUCT_PIPE;
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_identificador automático**](auto-handle.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**descodificar**](decode.md)
</dt> <dt>

[**codificar**](encode.md)
</dt> <dt>

[**enumeración**](enum.md)
</dt> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[**de**](in.md)
</dt> <dt>

[**objeto**](object.md)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**representar \_ como**](represent-as.md)
</dt> <dt>

[**Destructor**](struct.md)
</dt> <dt>

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**espeficarse**](unique.md)
</dt> <dt>

[**\_serialización de usuario**](user-marshal.md)
</dt> <dt>

[**\_serialización de cable**](wire-marshal.md)
</dt> </dl>

 

 