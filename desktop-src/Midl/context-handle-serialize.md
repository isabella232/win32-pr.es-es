---
title: context_handle_serialize atributo)
description: El atributo \ context \_ Handle \_ SERIALIZE \ ACF garantiza que siempre se serializará un identificador de contexto, independientemente del comportamiento predeterminado de la aplicación.
ms.assetid: e2f48582-228a-4725-9543-1e638d86ff6b
keywords:
- context_handle_serialize el atributo MIDL
topic_type:
- apiref
api_name:
- context_handle_serialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74e364c3ae8bf0439e50ae53130542762f37484
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105685694"
---
# <a name="context_handle_serialize-attribute"></a>\_atributo Serialize del controlador de contexto \_

El atributo **\[ identificador de contexto \_ \_ Serialize \]** de serialización garantiza que siempre se serializará un identificador de contexto, independientemente del comportamiento predeterminado de la aplicación.

``` syntax
typedef [context_handle_serialize [ , type-acf-attribute-list ] ] context-handle-type;

[context_handle_serialize [, function-acf-attribute-list ] ] function-name( );

function-name(
    [context_handle_serialize [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo-ACF-atributo-lista* 
</dt> <dd>

Cualquier otro atributo ACF que se aplique al tipo.

</dd> <dt>

*context-Handle-type* 
</dt> <dd>

El identificador que especifica el tipo de identificador de contexto, tal y como se define en una declaración [**typedef**](typedef.md) . Este es el tipo que recibe el atributo **\[ \_ \_ Serialize \] de identificador de contexto** en el archivo IDL.

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

El atributo **\[ \_ \_ Serialize \] del controlador de contexto** identifica un identificador de enlace que mantiene la información de contexto o de estado en el servidor entre las llamadas a procedimiento remoto. El atributo puede aparecer como un atributo de tipo [**typedef**](typedef.md) de IDL, como un atributo de tipo de valor devuelto de función, o como un atributo de parámetro.

De forma predeterminada, las llamadas a los identificadores de contexto se serializan, pero una aplicación puede llamar a [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) para invalidar este comportamiento predeterminado. El uso del atributo **\[ \_ \_ Serialize \] de identificador de contexto** en un archivo ACF garantiza que las llamadas en este identificador de contexto determinado se serializarán, incluso si la aplicación que realiza la llamada ha invalidado la serialización predeterminada. Una rutina de informe detallado de contexto es opcional.

Este atributo está disponible en la versión 5,0 de MIDL.

**Windows server 2003 y Windows XP o posterior:** Una sola interfaz puede alojar identificadores de contexto serializados y no serializados, lo que permite que un método de una interfaz tenga acceso a un identificador de contexto exclusivamente (serializado), mientras que otros métodos tienen acceso a ese identificador de contexto en modo compartido (no serializado). Estas capacidades de acceso son comparables a los mecanismos de bloqueo de lectura y escritura. los métodos que usan un identificador de contexto serializado son usuarios exclusivos (escritores), mientras que los métodos que usan un identificador de contexto no serializado son usuarios compartidos (lectores). Se deben serializar los métodos que destruyen o modifican el estado de un identificador de contexto. Los métodos que no modifican el estado de un identificador de contexto, como los métodos que simplemente leen un identificador de contexto, pueden ser no serializados. Tenga en cuenta que los métodos de creación se serializan implícitamente.

## <a name="examples"></a>Ejemplos

``` syntax
typedef [context_handle_serialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_serialize] pCxHandle);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[Atributos ACF](acf-attributes.md)
</dt> <dt>

[**identificador de contexto de \_ \_ noserialización**](context-handle-noserialize.md)
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

 

 