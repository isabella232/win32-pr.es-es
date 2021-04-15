---
title: transmit_as (atributo)
description: El atributo \ Transmit \_ as indica al compilador que asocie el tipo de identificador, que es un tipo presentado que las aplicaciones cliente y de servidor manipulan, con un tipo de transmisión de tipos transmitidos.
ms.assetid: 3dd1a242-03ec-49b4-ac96-87ef186e41d2
keywords:
- transmit_as el atributo MIDL
topic_type:
- apiref
api_name:
- transmit_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ec0cba27e994f7d77d441aef7bb783cad71cbad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665782"
---
# <a name="transmit_as-attribute"></a>transmitir \_ como atributo

El atributo **\[ Transmit \_ as \]** indica al compilador que asocie **type-id ** * *, que es un tipo presentado que las aplicaciones cliente y de servidor manipulan, con un tipo **de transmisión de** tipos transmitido.

``` syntax
typedef [transmit_as(xmit-type) [[ , type-attribute-list ]] ] type-specifier declarator-list; 

void __RPC_USER type-id_to_xmit (
  type-id __RPC_FAR *,
  xmit-type __RPC_FAR * __RPC_FAR *);
void __RPC_USER type-id_from_xmit (
  xmit-type __RPC_FAR *,
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_inst (
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_xmit (
  xmit-type__RPC_FAR *);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo de transmisión* 
</dt> <dd>

Especifica el tipo de datos que se transmite entre el cliente y el servidor.

</dd> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica uno o más atributos que se aplican al tipo. Entre los atributos de tipo válidos se incluyen **\[** el [**identificador**](handle.md) **\]** , **\[** el [**\_ tipo de conmutador**](switch-type.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** y la cadena de atributos de uso **\[** [](string.md) **\]** y **\[** [**omitir**](ignore.md) **\]** . Separe varios atributos con comas.

</dd> <dt>

*Type-Specifier* 
</dt> <dd>

Especifica un [tipo base](midl-base-types.md), un [**struct**](struct.md), una [**Unión**](union.md), un tipo de [**enumeración**](enum.md) o un identificador de tipo. Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.

</dd> <dt>

*lista de declaradores* 
</dt> <dd>

Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers). La *lista de declaradores* consta de uno o varios declaradores separados por comas. El declarador de parámetro del declarador de la función, como el nombre del parámetro, es opcional.

</dd> <dt>

*identificador de tipo* 
</dt> <dd>

Especifica el nombre del tipo de datos que se presenta a las aplicaciones de cliente y de servidor.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para usar el atributo **\[ Transmit \_ as \]** , el usuario debe proporcionar rutinas que conviertan datos entre los tipos presentados y transmitidos; estas rutinas también deben liberar la memoria que se usa para contener los datos convertidos. El atributo **\[ Transmit \_ as \]** indica al código auxiliar que llame a las rutinas de conversión proporcionadas por el usuario.

El tipo *de transmisión de* tipos transmitidos debe resolverse en un tipo base de MIDL, un tipo predefinido o un identificador de tipo. Para obtener más información, vea [tipos base de MIDL](midl-base-types.md).

El usuario debe proporcionar las rutinas siguientes.



| Nombre de rutina              | Descripción                                                                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Type-ID * * * \_ para la \_ transmisión**   | Convierte los datos del tipo presentado al tipo transmitido. Esta rutina asigna memoria para el tipo transmitido y para los datos a los que hacen referencia los punteros en el tipo transmitido.                            |
| *ID. de tipo * * * \_ de \_ transmisión** | Convierte los datos del tipo transmitido al tipo presentado. Esta rutina es responsable de la asignación de memoria para los datos a los que hacen referencia los punteros en el tipo presentado. RPC asigna memoria para el propio tipo. |
| *ID. de tipo * * \_ * \_ inst.** | Libera la memoria asignada para los datos a los que hacen referencia los punteros en el tipo presentado. RPC libera memoria para el propio tipo.                                                                                               |
| *tipo-ID * * * \_ \_ transmisión gratuita** | Libera el almacenamiento utilizado por el llamador para el tipo transmitido y para los datos a los que hacen referencia los punteros en el tipo transmitido.                                                                                            |



 

 

El código auxiliar del cliente llama al *ID. de tipo * * * \_ para la \_ transmisión** para asignar espacio para el tipo transmitido y para traducir los datos en objetos de tipo *tipo de transmisión.* El código auxiliar del servidor asigna espacio para el tipo de datos original y llama al *identificador de tipo * * * \_ desde \_ transmisión** para traducir los datos de su tipo transmitido al tipo presentado.

Al volver del código de la aplicación, el código auxiliar del servidor llama a *type-id * * * \_ Free \_ inst** para desasignar el almacenamiento para el ID. de *tipo* en el lado del servidor. El código auxiliar del cliente llama al *identificador de tipo * * * \_ \_ transmisión gratuita** para desasignar el almacenamiento del *tipo de transmisión* en el lado cliente.

Los tipos siguientes no pueden tener un atributo de **\[ transmisión \_ como \]** :

-   Identificadores de contexto (tipos con el atributo de tipo de **\[** [**\_ identificador de contexto**](context-handle.md) **\]** y los tipos que se usan como parámetros con el atributo de **\[ \_ identificador \] de contexto** )
-   Tipos que se canalizan o derivan de canalizaciones
-   Tipos de datos que se usan como tipo base de una definición de canalización
-   Parámetros que son punteros o se resuelven en punteros
-   Parámetros que son compatibles, variables o matrices de apertura
-   Estructuras que contienen matrices compatibles
-   Identificador de tipo predefinido [**\_ t**](handle-t.md), [**void**](void.md)

Los tipos que se transmiten deben cumplir las restricciones siguientes:

-   No deben ser punteros ni contener punteros.
-   No deben ser canalizaciones ni contener canalizaciones.

## <a name="examples"></a>Ejemplos

``` syntax
typedef struct _TREE_NODE_TYPE 
{ 
    unsigned short data; 
    struct _TREE_NODE_TYPE * left; 
    struct _TREE_NODE_TYPE * right; 
} TREE_NODE_TYPE; 
 
typedef [transmit_as(TREE_XMIT_TYPE)] TREE_NODE_TYPE * TREE_TYPE; 
 
void __RPC_USER TREE_TYPE_to_xmit( 
    TREE_TYPE __RPC_FAR * , 
    TREE_XMIT_TYPE __RPC_FAR * __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_from_xmit ( 
    TREE_XMIT_TYPE __RPC_FAR *, 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_inst( 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_xmit( 
    TREE_XMIT_TYPE __RPC_FAR *);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**matrices**](arrays-1.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**enumeración**](enum.md)
</dt> <dt>

[**asa**](handle.md)
</dt> <dt>

[**identificador \_ t**](handle-t.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**omitir**](ignore.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**Destructor**](struct.md)
</dt> <dt>

[**tipo de conmutador \_**](switch-type.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**Unión**](union.md)
</dt> <dt>

[**espeficarse**](unique.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 