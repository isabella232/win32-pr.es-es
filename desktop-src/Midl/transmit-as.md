---
title: transmit_as (atributo)
description: El atributo \transmit as\ indica al compilador que asocie type-id, que es un tipo presentado que las aplicaciones cliente y servidor manipulan, con un tipo \_ transmitido xmit-type.
ms.assetid: 3dd1a242-03ec-49b4-ac96-87ef186e41d2
keywords:
- transmit_as atributo MIDL
topic_type:
- apiref
api_name:
- transmit_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d1b8e9aae9a147c929fade8030babbf6b02fd87c9170370252522001742e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382836"
---
# <a name="transmit_as-attribute"></a>transmitir \_ como atributo

El **\[ atributo transmit \_ as \]** indica al compilador que asocie **type-id**_,_ que es un tipo presentado que las aplicaciones cliente y servidor manipulan, con un tipo **transmitido xmit-type.**

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

*xmit-type* 
</dt> <dd>

Especifica el tipo de datos que se transmite entre el cliente y el servidor.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Especifica uno o varios atributos que se aplican al tipo. Los atributos de tipo válidos incluyen el identificador , el tipo de modificador ; el atributo de puntero ref , unique o ptr ; y la **\[** [](handle.md) **\]** cadena de atributos **\[** [**\_**](switch-type.md) **\]** de uso **\[** [](ref.md) **\]** **\[** [](unique.md) **\]** y **\[** [](ptr.md) **\]** **\[** [](string.md) **\]** **\[** [**omiten**](ignore.md) **\]** . Separe varios atributos con comas.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Especifica un tipo [base,](midl-base-types.md) [**struct**](struct.md), [**union,**](union.md) [**tipo de enumeración**](enum.md) o identificador de tipo. Una especificación de almacenamiento opcional puede *preceder al especificador de tipo*.

</dd> <dt>

*declarator-list* 
</dt> <dd>

Especifica declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers). La *lista de declaradores* consta de uno o varios declaradores separados por comas. El declarador de parámetros del declarador de función, como el nombre del parámetro, es opcional.

</dd> <dt>

*type-id* 
</dt> <dd>

Especifica el nombre del tipo de datos que se presenta a las aplicaciones cliente y servidor.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para usar el atributo **\[ transmitir \_ \]** como , el usuario debe proporcionar rutinas que conviertan datos entre los tipos presentados y transmitidos; estas rutinas también deben liberar memoria usada para contener los datos convertidos. El **\[ atributo transmit \_ as \]** indica a los códigos auxiliares que llamen a las rutinas de conversión proporcionadas por el usuario.

El tipo transmitido *xmit-type* debe resolverse en un tipo base MIDL, un tipo predefinido o un identificador de tipo. Para obtener más información, vea [MidL Base Types](midl-base-types.md).

El usuario debe proporcionar las rutinas siguientes.



| Nombre de rutina              | Descripción                                                                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *type-id: \_ para \_ xmit**   | Convierte los datos del tipo presentado al tipo transmitido. Esta rutina asigna memoria para el tipo transmitido y para los datos a los que hacen referencia los punteros del tipo transmitido.                            |
| *type-id% \_ de \_ xmit** | Convierte los datos del tipo transmitido al tipo presentado. Esta rutina es responsable de asignar memoria para los datos a los que hacen referencia los punteros en el tipo presentado. RPC asigna memoria para el propio tipo. |
| *type-id" \_ free \_ inst** | Libera la memoria asignada para los datos a los que hacen referencia los punteros en el tipo presentado. RPC libera memoria para el propio tipo.                                                                                               |
| *type-id: \_ \_ xmit gratis** | Libera el almacenamiento utilizado por el autor de la llamada para el tipo transmitido y para los datos a los que hacen referencia los punteros del tipo transmitido.                                                                                            |



 

 

El código auxiliar de cliente llama *a type-id** para \_ \_ xmit** para asignar espacio para el tipo transmitido y traducir los datos en objetos de tipo *xmit-type.* El código auxiliar del servidor asigna espacio para el tipo de datos original y llama a *type-id** desde \_ \_ xmit** para traducir los datos de su tipo transmitido al tipo presentado.

Tras la devolución del código de aplicación, el código auxiliar del servidor llama a *type-id+ \_ free \_ inst** para desasignar el almacenamiento para *type-id* en el lado servidor. El código auxiliar de cliente llama *a type-id+ \_ \_ xmit** gratis para desasignar el almacenamiento *de tipo xmit* en el lado cliente.

Los siguientes tipos no pueden tener un **\[ atributo transmit \_ as: \]**

-   Identificadores de contexto (tipos con el atributo de tipo de identificador de contexto y **\[** tipos que se usan como parámetros con el atributo de identificador [**\_**](context-handle.md) **\]** **\[ \_ de \]** contexto)
-   Tipos que son canalizaciones o derivadas de canalizaciones
-   Tipos de datos que se usan como tipo base de una definición de canalización
-   Parámetros que son punteros o se resuelven como punteros
-   Parámetros que son matrices compatibles, variables o abiertas
-   Estructuras que contienen matrices conformes
-   El identificador de tipo [**predefinido \_ t**](handle-t.md), [**void**](void.md)

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

[**Matrices**](arrays-1.md)
</dt> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**identificador de \_ contexto**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**handle**](handle.md)
</dt> <dt>

[**handle \_ t**](handle-t.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Ignorar**](ignore.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Cadena**](string.md)
</dt> <dt>

[**Estructura**](struct.md)
</dt> <dt>

[**tipo \_ de conmutador**](switch-type.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Unión**](union.md)
</dt> <dt>

[**Único**](unique.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 