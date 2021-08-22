---
title: context_handle_noserialize atributo
description: El atributo \_ \context handle noserialize\ ACF garantiza que un identificador de contexto nunca se serializará, independientemente del comportamiento predeterminado \_ de la aplicación.
ms.assetid: aff2484e-639b-41d2-94a9-f34ca4f2343c
keywords:
- context_handle_noserialize atributo MIDL
topic_type:
- apiref
api_name:
- context_handle_noserialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40556db0d63441e42d46a0ed7f9bd45edb8b2ce65f8d4b9b84e3a848325ddbb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014003"
---
# <a name="context_handle_noserialize-attribute"></a>atributo \_ \_ noserialize del identificador de contexto

El **\[ atributo \_ \_ ACF noserialize \]** del identificador de contexto garantiza que nunca se serializará un identificador de contexto, independientemente del comportamiento predeterminado de la aplicación.

``` syntax
typedef [context_handle_noserialize [ , type-acf-attribute-list ] ] context-handle-type

[context_handle_noserialize [, function-acf-attribute-list ] ] function-name( );

function-name (   [context_handle_noserialize 
  [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*type-acf-attribute-list* 
</dt> <dd>

Cualquier otro atributo de ACF que se aplique al tipo.

</dd> <dt>

*context-handle-type* 
</dt> <dd>

Identificador que especifica el tipo de identificador de contexto, tal como se define en una [**declaración typedef.**](typedef.md) Este es el tipo que recibe el atributo [**\[ de identificador \_ de \]**](context-handle.md) contexto en el archivo IDL.

</dd> <dt>

*function-acf-attribute-list* 
</dt> <dd>

Cualquier atributo ACF adicional que se aplique a la función.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Nombre de la función tal como se define en el archivo IDL.

</dd> <dt>

*parameter-acf-attribute-list* 
</dt> <dd>

Cualquier otro atributo ACF que se aplique al parámetro .

</dd> <dt>

*param-name* 
</dt> <dd>

Nombre del parámetro tal como se define en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El [**\[ atributo de \_ identificador \]**](context-handle.md) de contexto identifica un identificador de enlace que mantiene el contexto o la información de estado en el servidor entre llamadas a procedimiento remoto. El atributo puede aparecer como un atributo de tipo [**typedef**](typedef.md) de IDL, como un atributo de tipo de valor devuelto de función o como un atributo de parámetro.

De forma predeterminada, se serializan las llamadas en los identificadores de contexto. Una aplicación puede llamar a [**RpcSsDontSerializeContext para**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) invalidar este comportamiento predeterminado. El uso [**\[ del atributo \_ de \]**](context-handle.md) identificador de contexto en un archivo ACF garantiza que las llamadas en este identificador de contexto determinado no se serializarán, independientemente del comportamiento de la aplicación que realiza la llamada. Proporcionar una rutina de desmontaje de contexto es opcional.

Este atributo está disponible en MIDL versión 5.0.

**Windows ServerÂ 2003 y Windows XP o posterior:** Una única interfaz puede dar cabida a identificadores de contexto serializados y no serializados, lo que permite que un método de una interfaz acceda exclusivamente a un identificador de contexto (serializado), mientras que otros métodos acceden a ese identificador de contexto en modo compartido (no serializado). Estas funcionalidades de acceso son comparables a los mecanismos de bloqueo de lectura y escritura. Los métodos que usan un identificador de contexto serializado son usuarios exclusivos (escritores), mientras que los métodos que usan un identificador de contexto no serializado son usuarios compartidos (lectores). Se deben serializar los métodos que destruyen o modifican el estado de un identificador de contexto. Los métodos que no modifican el estado de un identificador de contexto, como los métodos que simplemente leen de un identificador de contexto, pueden no serializarse. Tenga en cuenta que los métodos de creación se serializan implícitamente.

## <a name="examples"></a>Ejemplos

``` syntax
typedef [context_handle_noserialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_noserialize] pCxHandle);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos de ACF](acf-attributes.md)
</dt> <dt>

[**serialización \_ del \_ identificador de contexto**](context-handle-serialize.md)
</dt> <dt>

[**identificador de \_ contexto**](context-handle.md)
</dt> <dt>

[Identificadores de contexto](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[Rutina de ejecución de contexto de servidor](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[Clientes multiproceso y identificadores de contexto](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 