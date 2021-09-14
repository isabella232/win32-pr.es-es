---
title: context_handle atributo
description: El atributo \ context handle\ identifica un identificador de enlace que mantiene el contexto o la información de estado en el servidor entre \_ llamadas a procedimiento remoto.
ms.assetid: ab1aee44-4add-4816-a7ef-38bbf7b38918
keywords:
- context_handle atributo MIDL
topic_type:
- apiref
api_name:
- context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71c47554454118d584110ec43211a302e12cd77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159646"
---
# <a name="context_handle-attribute"></a>atributo de \_ identificador de contexto

El **\[ atributo de \_ identificador \]** de contexto identifica un identificador de enlace que mantiene el contexto o la información de estado en el servidor entre llamadas a procedimiento remoto.

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

*type-attribute-list* 
</dt> <dd>

Especifica uno o varios atributos que se aplican al tipo.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Especifica un tipo de puntero o un identificador de tipo. Una especificación de almacenamiento opcional puede *preceder al especificador de tipo*.

</dd> <dt>

*declarator y declarator-list* 
</dt> <dd>

Especifica declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. El declarador de un identificador de contexto debe incluir al menos un declarador de puntero. Para obtener más información, vea [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers). La *lista de declaradores* consta de uno o varios declaradores, separados por comas. El identificador de nombre de parámetro en el declarador de función es opcional.

</dd> <dt>

*function-attr-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son la devolución de llamada , local; el atributo de puntero **\[** [](callback.md) **\]** **\[** [](local.md) **\]** **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md); **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[ \_ \]** y la cadena de atributos de uso , ignore y el identificador de contexto .

</dd> <dt>

*ptr-decl* 
</dt> <dd>

Especifica cero o más declaradores de puntero. Un declarador de puntero es el mismo que el declarador de puntero usado en C; se construye a partir del **\* *designador _ , modificadores como _* far** y el calificador [**const**](const.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Especifica cero o más atributos direccionales, atributos de campo, atributos de uso y atributos de puntero adecuados para el tipo de parámetro especificado. Separe varios atributos con comas.

</dd> <dt>

*context-handle-type* 
</dt> <dd>

Especifica el identificador que especifica el tipo de identificador de contexto tal como se define en una declaración [**typedef**](typedef.md) que toma el atributo **\[ de identificador \_ de \]** contexto. La rutina de desmontaje es opcional.

**Windows ServerÂ 2003 y Windows XP:** Una única interfaz puede dar cabida a identificadores de contexto serializados y no serializados, lo que permite que un método de una interfaz acceda exclusivamente a un identificador de contexto (serializado), mientras que otros métodos acceden a ese identificador de contexto en modo compartido (no serializado). Estas funcionalidades de acceso son comparables a los mecanismos de bloqueo de lectura y escritura. Los métodos que usan un identificador de contexto serializado son usuarios exclusivos (escritores), mientras que los métodos que usan un identificador de contexto no serializado son usuarios compartidos (lectores). Se deben serializar los métodos que destruyen o modifican el estado de un identificador de contexto. Los métodos que no modifican el estado de un identificador de contexto, como los métodos que simplemente leen de un identificador de contexto, pueden no serializarse. Tenga en cuenta que los métodos de creación se serializan implícitamente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ atributo de \_ identificador \]** de contexto puede aparecer como un atributo de tipo [**typedef**](typedef.md) de IDL, como un atributo de tipo de valor devuelto de función o como un atributo de parámetro. Al aplicar el atributo **\[ de identificador \_ de \]** contexto a una definición de tipo, también debe proporcionar una rutina de resumen de contexto. Consulte [Rutina de ejecución de contexto de servidor para](/windows/desktop/Rpc/server-context-run-down-routine) obtener más información.

Cuando se usa el compilador MIDL en modo predeterminado ([**/ms \_ ext**](-ms-ext.md)), un identificador de contexto puede ser cualquier tipo de puntero seleccionado por el usuario, siempre que cumpla los requisitos de identificadores de contexto que se describen aquí. Los datos asociados a este tipo de identificador de contexto no se transmiten en la red y solo deben ser manipulados por la aplicación de servidor. Los compiladores IDL de DCE restringen los identificadores de contexto a punteros de tipo [**void**](void.md)  * *\** _. Por lo tanto, esta característica no está disponible cuando se usa el modificador [*/osf* * del](-osf.md) compilador midL.

Al igual que con otros tipos de identificador, el identificador de contexto es opaco para la aplicación cliente y no se transmiten los datos asociados a él. En el servidor, el identificador de contexto actúa como identificador en el contexto activo y se puede acceder a todos los datos asociados con el tipo de identificador de contexto.

Para crear un identificador de contexto, el cliente pasa al servidor un **\[** [**puntero out**](out-idl.md) **\]** , **\[** [**ref**](ref.md) a un identificador **\]** de contexto. (El propio identificador de contexto puede tener un valor **NULL** o no **NULL,** siempre que su valor sea coherente con sus atributos de puntero. Por ejemplo, cuando el tipo de identificador de contexto tiene aplicado el atributo **\[** [**ref,**](ref.md) **\]** no puede tener un valor **NULL).** Se debe proporcionar otro identificador de enlace para realizar el enlace hasta que se cree el identificador de contexto. Cuando no se especifica ningún identificador explícito, se usa el enlace implícito. Cuando no **\[** [**hay ningún atributo \_ de**](implicit-handle.md) **\]** identificador implícito, se usa un identificador automático.

El procedimiento remoto en el servidor crea un identificador de contexto activo. El cliente debe usar ese identificador de contexto como **\[** [**un parámetro in**](in.md) o **\]** **\[ en**, **out \]** en las llamadas posteriores. Un **\[ identificador \]** de contexto de solo en se puede usar como identificador de enlace, por lo que debe tener un valor distinto de **NULL.** Un **\[ identificador \]** de contexto solo en no refleja los cambios de estado en el servidor.

En el servidor, el procedimiento llamado puede interpretar el identificador de contexto según sea necesario. Por ejemplo, el procedimiento llamado puede asignar almacenamiento del montón y usar el identificador de contexto como puntero a este almacenamiento.

Para cerrar un identificador de contexto, el cliente pasa el identificador de contexto como **\[** [**un argumento en**](in.md), **\]** **\[** [](out-idl.md) **\]** out. El servidor debe devolver un **identificador de** contexto NULL cuando ya no mantiene el contexto en nombre del autor de la llamada. Por ejemplo, si el identificador de contexto representa un archivo abierto y la llamada cierra el archivo, el servidor debe establecer el identificador de contexto en **NULL** y devolverlo al cliente. Un **valor NULL** no es válido como identificador de enlace en llamadas posteriores.

Un identificador de contexto solo es válido para un servidor. Cuando una función tiene dos parámetros de identificador y el identificador de contexto no es **NULL**, los identificadores de enlace deben hacer referencia al mismo espacio de direcciones.

Cuando una función tiene un identificador de contexto en o en **\[** [](in.md) **\]** , **\[** **\]** su identificador de contexto se puede usar como identificador de enlace. En este caso, no se usa el enlace implícito y se omite el identificador **\[** [**\_ implícito**](implicit-handle.md) **\]** o el atributo de identificador **\[** [**\_**](auto-handle.md) **\]** automático.

Las restricciones siguientes se aplican a los identificadores de contexto:

-   Los identificadores de contexto no pueden ser elementos de matriz, miembros de estructura o miembros de unión. Solo pueden ser parámetros.
-   Los identificadores de contexto no pueden **\[** [**tener la transmisión \_ como**](transmit-as.md) **\]** o representar **\[** [**\_ como**](represent-as.md) **\]** atributo.
-   Los parámetros que son punteros a **\[** [](out-idl.md) **\]** identificadores de contexto de salida deben ser **\[** [**punteros**](ref.md) **\]** ref.
-   Un **\[** [**identificador**](in.md) **\]** en contexto se puede usar como identificador de enlace y no puede ser **NULL.**
-   En **\[ ,** el [**identificador de**](out-idl.md) contexto de salida puede ser **NULL en** la entrada, pero solo si el procedimiento tiene otro parámetro de identificador explícito. Si no hay ningún otro parámetro de identificador de contexto no **NULL** explícito, **en \[**, el identificador **\] de** contexto de salida no puede ser **NULL.**
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

[**Matrices**](arrays-1.md)
</dt> <dt>

[**identificador \_ automático**](auto-handle.md)
</dt> <dt>

[**devolución de llamada**](callback.md)
</dt> <dt>

[Restablecimiento del contexto de cliente](/windows/desktop/Rpc/client-context-reset)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Identificadores de contexto](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**handle**](handle.md)
</dt> <dt>

[Enlace y identificadores](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[**Ignorar**](ignore.md)
</dt> <dt>

[**identificador \_ implícito**](implicit-handle.md)
</dt> <dt>

[**En**](in.md)
</dt> <dt>

[**Local**](local.md)
</dt> <dt>

[Clientes multiproceso y identificadores de contexto](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**/ms \_ ext**](-ms-ext.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**representar \_ como**](represent-as.md)
</dt> <dt>

[**RpcSsDestroyClientContext**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdestroyclientcontext)
</dt> <dt>

[Rutina de ejecución de contexto de servidor](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[**Cadena**](string.md)
</dt> <dt>

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Único**](unique.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 