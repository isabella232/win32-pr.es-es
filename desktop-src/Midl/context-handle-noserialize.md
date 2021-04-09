---
title: context_handle_noserialize atributo)
description: El atributo \ context \_ Handle \_ noserialization \ ACF garantiza que nunca se serializará un identificador de contexto, independientemente del comportamiento predeterminado de la aplicación.
ms.assetid: aff2484e-639b-41d2-94a9-f34ca4f2343c
keywords:
- context_handle_noserialize el atributo MIDL
topic_type:
- apiref
api_name:
- context_handle_noserialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f3f2a72837df5efa3b74bd2672e39c3c3b12
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789873"
---
# <a name="context_handle_noserialize-attribute"></a>atributo de identificador de contexto \_ \_ noserialización

El atributo **\[ identificador de contexto \_ \_ noserializate \]** ACF garantiza que nunca se serializará un identificador de contexto, independientemente del comportamiento predeterminado de la aplicación.

``` syntax
typedef [context_handle_noserialize [ , type-acf-attribute-list ] ] context-handle-type

[context_handle_noserialize [, function-acf-attribute-list ] ] function-name( );

function-name (   [context_handle_noserialize 
  [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo-ACF-atributo-lista* 
</dt> <dd>

Cualquier otro atributo ACF que se aplique al tipo.

</dd> <dt>

*context-Handle-type* 
</dt> <dd>

El identificador que especifica el tipo de identificador de contexto, tal y como se define en una declaración [**typedef**](typedef.md) . Este es el tipo que recibe el atributo de [**\[ \_ identificador \] de contexto**](context-handle.md) en el archivo IDL.

</dd> <dt>

*function-ACF-Attribute-List* 
</dt> <dd>

Cualquier atributo ACF adicional que se aplique a la función.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Nombre de la función tal y como se define en el archivo IDL.

</dd> <dt>

*parámetro-ACF-Attribute-List* 
</dt> <dd>

Cualquier otro atributo ACF que se aplique al parámetro.

</dd> <dt>

*param: nombre* 
</dt> <dd>

Nombre del parámetro tal y como se define en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo de [**\[ \_ identificador \] de contexto**](context-handle.md) identifica un identificador de enlace que mantiene el contexto o la información de estado en el servidor entre las llamadas a procedimiento remoto. El atributo puede aparecer como un atributo de tipo [**typedef**](typedef.md) de IDL, como un atributo de tipo de valor devuelto de función, o como un atributo de parámetro.

De forma predeterminada, se serializan las llamadas en los identificadores de contexto. Una aplicación puede llamar a [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) para invalidar este comportamiento predeterminado. El uso del atributo de [**\[ \_ identificador \] de contexto**](context-handle.md) en un archivo ACF garantiza que las llamadas en este identificador de contexto determinado no se serializarán, independientemente del comportamiento de la aplicación que realiza la llamada. Proporcionar una rutina de Resumen de contexto es opcional.

Este atributo está disponible en la versión 5,0 de MIDL.

**Windows server 2003 y Windows XP o posterior:** Una sola interfaz puede alojar identificadores de contexto serializados y no serializados, lo que permite que un método de una interfaz tenga acceso a un identificador de contexto exclusivamente (serializado), mientras que otros métodos tienen acceso a ese identificador de contexto en modo compartido (no serializado). Estas capacidades de acceso son comparables a los mecanismos de bloqueo de lectura y escritura. los métodos que usan un identificador de contexto serializado son usuarios exclusivos (escritores), mientras que los métodos que usan un identificador de contexto no serializado son usuarios compartidos (lectores). Se deben serializar los métodos que destruyen o modifican el estado de un identificador de contexto. Los métodos que no modifican el estado de un identificador de contexto, como los métodos que simplemente leen un identificador de contexto, pueden ser no serializados. Tenga en cuenta que los métodos de creación se serializan implícitamente.

## <a name="examples"></a>Ejemplos

``` syntax
typedef [context_handle_noserialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_noserialize] pCxHandle);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos ACF](acf-attributes.md)
</dt> <dt>

[**\_serializar identificador de contexto \_**](context-handle-serialize.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[Identificadores de contexto](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[Rutina de ejecución de contexto de servidor](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[Clientes multiproceso y controladores de contexto](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 