---
title: context_handle atributo)
description: El atributo \ context \_ handler identifica un identificador de enlace que mantiene el contexto o la información de estado en el servidor entre las llamadas a procedimiento remoto.
ms.assetid: ab1aee44-4add-4816-a7ef-38bbf7b38918
keywords:
- context_handle el atributo MIDL
topic_type:
- apiref
api_name:
- context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71c47554454118d584110ec43211a302e12cd77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789868"
---
# <a name="context_handle-attribute"></a>atributo de identificador de contexto \_

El atributo de **\[ \_ identificador \] de contexto** identifica un identificador de enlace que mantiene el contexto o la información de estado en el servidor entre las llamadas a procedimiento remoto.

``` syntax
typedef [context_handle [ , type-attribute-list ] ] type-specifier declarator-list;

[context_handle [, function-attr-list ] ] type-specifier [ptr-decl] function-name(
    [ [parameter-attribute-list] ] type-specifier [declarator], ...);

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [context_handle [ , parameter-attribute-list ] ] type-specifier [declarator], ...);

[ void __RPC_USER context-handle-type_rundown (
  context-handle-type); ]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica uno o más atributos que se aplican al tipo.

</dd> <dt>

*Type-Specifier* 
</dt> <dd>

Especifica un tipo de puntero o un identificador de tipo. Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.

</dd> <dt>

*declarador y lista de declaradores* 
</dt> <dd>

Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. El declarador de un identificador de contexto debe incluir al menos un declarador de puntero. Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers). La *lista de declaradores* consta de uno o varios declaradores, separados por comas. El identificador de nombre de parámetro en el declarador de función es opcional.

</dd> <dt>

*function-ATTR-List* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y los atributos de uso **\[** [**cadena**](string.md) **\]** , **\[** [**omitir**](ignore.md) **\]** y **\[ \_ identificador \] de contexto**.

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Especifica cero o más declaradores de puntero. Un declarador de puntero es el mismo que el declarador de puntero utilizado en C; se construye a partir del **\*** designador, modificadores como **Far** y el calificador [**const**](const.md).

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Especifica cero o más atributos direccionales, atributos de campo, atributos de uso y atributos de puntero adecuados para el tipo de parámetro especificado. Separe varios atributos con comas.

</dd> <dt>

*context-Handle-type* 
</dt> <dd>

Especifica el identificador que especifica el tipo de identificador de contexto tal y como se define en una declaración [**typedef**](typedef.md) que toma el atributo de **\[ \_ identificador \] de contexto** . La rutina de informe detallado es opcional.

**Windows server 2003 y Windows XP:** Una sola interfaz puede alojar identificadores de contexto serializados y no serializados, lo que permite que un método de una interfaz tenga acceso a un identificador de contexto exclusivamente (serializado), mientras que otros métodos tienen acceso a ese identificador de contexto en modo compartido (no serializado). Estas capacidades de acceso son comparables a los mecanismos de bloqueo de lectura y escritura. los métodos que usan un identificador de contexto serializado son usuarios exclusivos (escritores), mientras que los métodos que usan un identificador de contexto no serializado son usuarios compartidos (lectores). Se deben serializar los métodos que destruyen o modifican el estado de un identificador de contexto. Los métodos que no modifican el estado de un identificador de contexto, como los métodos que simplemente leen un identificador de contexto, pueden ser no serializados. Tenga en cuenta que los métodos de creación se serializan implícitamente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo de **\[ \_ identificador \] de contexto** puede aparecer como un atributo de tipo [**typedef**](typedef.md) de IDL, como un atributo de tipo de valor devuelto de función o como atributo de parámetro. Al aplicar el atributo de **\[ \_ identificador \] de contexto** a una definición de tipo, también debe proporcionar una rutina de Resumen de contexto. Vea [rutina de ejecución de contexto de servidor](/windows/desktop/Rpc/server-context-run-down-routine) para obtener más información.

Cuando se usa el compilador MIDL en modo predeterminado ([**/MS \_ ext**](-ms-ext.md)), un identificador de contexto puede ser cualquier tipo de puntero seleccionado por el usuario, siempre que cumpla los requisitos de los identificadores de contexto que se describen aquí. Los datos asociados a este tipo de identificador de contexto no se transmiten en la red y solo la aplicación de servidor debe manipularlos. Los compiladores de DCE IDL restringen los identificadores de contexto a punteros de tipo [**void**](void.md) **\*** . Por lo tanto, esta característica no está disponible cuando se usa el modificador [**/OSF**](-osf.md) del compilador MIDL.

Como con otros tipos de identificadores, el identificador de contexto es opaco para la aplicación cliente y no se transmite ningún dato asociado a él. En el servidor, el identificador de contexto actúa como un identificador en el contexto activo y se puede tener acceso a todos los datos asociados al tipo de identificador de contexto.

Para crear un identificador de contexto, el cliente pasa al servidor un **\[** puntero [**out**](out-idl.md) **\]** , **\[** [**ref**](ref.md) **\]** a un identificador de contexto. (El propio identificador de contexto puede tener un valor **null** o distinto de **null** , siempre que su valor sea coherente con sus atributos de puntero. Por ejemplo, cuando el tipo de identificador de contexto tiene **\[** [](ref.md) **\]** aplicado el atributo ref, no puede tener un valor **null** . Se debe proporcionar otro identificador de enlace para realizar el enlace hasta que se cree el identificador de contexto. Cuando no se especifica ningún identificador explícito, se utiliza el enlace implícito. Cuando no hay ningún **\[** atributo de [**\_ identificador implícito**](implicit-handle.md) **\]** presente, se utiliza un identificador automático.

El procedimiento remoto en el servidor crea un identificador de contexto activo. El cliente debe utilizar ese identificador de contexto como un **\[** [](in.md) **\]** parámetro in o **\[ in**, **out \]** en las llamadas posteriores. Un identificador **\[ \] de** contexto solo se puede usar como identificador de enlace, por lo que debe tener un valor distinto de **null** . Un identificador **\[ de contexto de solo en \]** no refleja los cambios de estado en el servidor.

En el servidor, el procedimiento llamado puede interpretar el identificador de contexto según sea necesario. Por ejemplo, el procedimiento llamado puede asignar almacenamiento de montón y usar el identificador de contexto como un puntero a este almacenamiento.

Para cerrar un identificador de contexto, el cliente pasa el identificador de contexto como un **\[** argumento [**in**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** . El servidor debe devolver un identificador de contexto **nulo** cuando ya no se mantiene el contexto en nombre del autor de la llamada. Por ejemplo, si el identificador de contexto representa un archivo abierto y la llamada cierra el archivo, el servidor debe establecer el identificador de contexto en **null** y devolverlo al cliente. Un valor **null** no es válido como un controlador de enlace en las llamadas subsiguientes.

Un identificador de contexto solo es válido para un servidor. Cuando una función tiene dos parámetros de identificador y el identificador de contexto no es **null**, los identificadores de enlace deben hacer referencia al mismo espacio de direcciones.

Cuando una función tiene un **\[** [**en**](in.md) **\]** o un identificador **\[ de contexto de** **salida \]** , su identificador de contexto se puede usar como identificador de enlace. En este caso, no se utiliza el enlace implícito y **\[** se omite el [**\_ identificador implícito**](implicit-handle.md) **\]** o el atributo de **\[** [**\_ identificador automático**](auto-handle.md) **\]** .

Las restricciones siguientes se aplican a los identificadores de contexto:

-   Los identificadores de contexto no pueden ser elementos de matriz, miembros de estructura o miembros de Unión. Solo pueden ser parámetros.
-   Los identificadores de contexto no pueden tener el **\[** atributo [**transmitir \_ como**](transmit-as.md) **\]** o **\[** [**representar \_ como**](represent-as.md) **\]** .
-   Los parámetros que son punteros a **\[** [](out-idl.md) **\]** identificadores de contexto de salida deben ser **\[** [](ref.md) **\]** punteros de referencia.
-   Se **\[** [](in.md) **\]** puede usar un en el identificador de contexto como identificador de enlace y no puede ser **null**.
-   En, un identificador **\[ de contexto de** [**salida**](out-idl.md) puede ser **null** en la entrada, pero solo si el procedimiento tiene otro parámetro de identificador explícito. Si no hay ningún otro parámetro **\[ de identificador de** contexto no **nulo** explícito, el identificador de contexto de **salida \]** no puede ser **null**.
-   No se puede usar un identificador de contexto con devoluciones de llamada.

## <a name="examples"></a>Ejemplos

``` syntax
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE; 
short RemoteFunc1([out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
short RemoteFunc2([in, out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown (PCONTEXT_HANDLE_TYPE);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**matrices**](arrays-1.md)
</dt> <dt>

[**\_identificador automático**](auto-handle.md)
</dt> <dt>

[**devolución de llamada**](callback.md)
</dt> <dt>

[Restablecimiento de contexto de cliente](/windows/desktop/Rpc/client-context-reset)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Identificadores de contexto](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**asa**](handle.md)
</dt> <dt>

[Enlace y controladores](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[**omitir**](ignore.md)
</dt> <dt>

[**\_identificador implícito**](implicit-handle.md)
</dt> <dt>

[**de**](in.md)
</dt> <dt>

[**localizar**](local.md)
</dt> <dt>

[Clientes multiproceso y controladores de contexto](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**\_ext/MS**](-ms-ext.md)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**representar \_ como**](represent-as.md)
</dt> <dt>

[**RpcSsDestroyClientContext**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdestroyclientcontext)
</dt> <dt>

[Rutina de ejecución de contexto de servidor](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**espeficarse**](unique.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 