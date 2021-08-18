---
title: context_handle_serialize atributo
description: El atributo \ context \_ handle serialize\ ACF garantiza que siempre se serializará un identificador de contexto, independientemente del comportamiento predeterminado \_ de la aplicación.
ms.assetid: e2f48582-228a-4725-9543-1e638d86ff6b
keywords:
- context_handle_serialize atributo MIDL
topic_type:
- apiref
api_name:
- context_handle_serialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91bf9ab1610585001b1380b15ba5a89433f80194596e26cbae84692ff3a872a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013963"
---
# <a name="context_handle_serialize-attribute"></a>atributo de \_ \_ serialización del identificador de contexto

El atributo ACF **\[ \_ \_ de serialización \]** del identificador de contexto garantiza que un identificador de contexto siempre se serializará, independientemente del comportamiento predeterminado de la aplicación.

``` syntax
typedef [context_handle_serialize [ , type-acf-attribute-list ] ] context-handle-type;

[context_handle_serialize [, function-acf-attribute-list ] ] function-name( );

function-name(
    [context_handle_serialize [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*type-acf-attribute-list* 
</dt> <dd>

Cualquier otro atributo de ACF que se aplique al tipo.

</dd> <dt>

*context-handle-type* 
</dt> <dd>

Identificador que especifica el tipo de identificador de contexto, tal como se define en una [**declaración typedef.**](typedef.md) Este es el tipo que recibe el atributo **\[ \_ \_ de serialización \] del** identificador de contexto en el archivo IDL.

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

Cualquier otro atributo de ACF que se aplique al parámetro .

</dd> <dt>

*param-name* 
</dt> <dd>

Nombre del parámetro tal como se define en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **\[ atributo de \_ \_ serialización del \]** identificador de contexto identifica un identificador de enlace que mantiene información de contexto o estado en el servidor entre llamadas a procedimiento remoto. El atributo puede aparecer como un atributo de tipo [**typedef**](typedef.md) de IDL, como un atributo de tipo de valor devuelto de función o como un atributo de parámetro.

De forma predeterminada, las llamadas en identificadores de contexto se serializan, pero una aplicación puede llamar a [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) para invalidar este comportamiento predeterminado. El uso del atributo **\[ \_ \_ de \]** serialización del identificador de contexto en un archivo ACF garantiza que las llamadas a en este identificador de contexto determinado se serializarán, incluso si la aplicación que realiza la llamada ha invalidado la serialización predeterminada. Una rutina de desmontaje de contexto es opcional.

Este atributo está disponible en MIDL versión 5.0.

**Windows ServerÂ 2003 y Windows XP o posterior:** Una sola interfaz puede dar cabida a identificadores de contexto serializados y no serializados, lo que permite que un método de una interfaz acceda exclusivamente a un identificador de contexto (serializado), mientras que otros métodos acceden a ese identificador de contexto en modo compartido (no serializado). Estas funcionalidades de acceso son comparables a los mecanismos de bloqueo de lectura y escritura. Los métodos que usan un identificador de contexto serializado son usuarios exclusivos (escritores), mientras que los métodos que usan un identificador de contexto no serializado son usuarios compartidos (lectores). Se deben serializar los métodos que destruyen o modifican el estado de un identificador de contexto. Los métodos que no modifican el estado de un identificador de contexto, como los métodos que simplemente leen de un identificador de contexto, pueden no serializarse. Tenga en cuenta que los métodos de creación se serializan implícitamente.

## <a name="examples"></a>Ejemplos

``` syntax
typedef [context_handle_serialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_serialize] pCxHandle);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[Atributos de ACF](acf-attributes.md)
</dt> <dt>

[**noserialize \_ del \_ identificador de contexto**](context-handle-noserialize.md)
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

 

 