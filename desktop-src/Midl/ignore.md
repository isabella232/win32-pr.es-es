---
title: ignore attribute
description: El atributo \ ignore\ designa que no se transmite un puntero contenido en una estructura o unión y el objeto indicado por el puntero. El atributo \ ignore\ está restringido a los miembros de puntero de estructuras o uniones.
ms.assetid: 9c2fc71a-4fac-4a59-95f5-2121067b326f
keywords:
- ignore attribute MIDL
topic_type:
- apiref
api_name:
- ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c6b7a1e70804bc3c9c277f3d46ac6a8ad20fc0f98b370f93fe9fd09b0b1bb99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013863"
---
# <a name="ignore-attribute"></a>ignore attribute

El **\[ atributo ignore \]** designa que no se transmite un puntero contenido en una estructura o unión y el objeto indicado por el puntero. El **\[ atributo ignore \]** está restringido a los miembros de puntero de estructuras o uniones.

``` syntax
[ignore] pointer-member-type pointer-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*pointer-member-type* 
</dt> <dd>

Especifica el tipo del miembro de puntero de la estructura o unión.

</dd> <dt>

*pointer-name* 
</dt> <dd>

Especifica el nombre del miembro de puntero que se omitirá durante la serialización.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El valor de un miembro de estructura con el **\[ atributo ignore \]** no está definido en el destino. No **\[** [**se**](in.md) **\]** define un parámetro in en el equipo remoto. No **\[** [**se**](out-idl.md) **\]** define un parámetro out en el equipo local.

El **\[ atributo ignore \]** permite evitar la transmisión de datos. Esto es útil en situaciones como una lista de doble vinculación. En el ejemplo siguiente se incluye una lista de doble vinculación que presenta el alias de datos:

``` syntax
/* IDL file */ 
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE; 
 
HRESULT remote_op([in] DBL_LINK_NODE_TYPE * list_head); 
 
/* application */ 
DBL_LINK_NODE_TYPE * p, * q 
 
p = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
q = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
 
p->next = q;  
q->previous = p; 
p->previous = q->next = NULL; 
.. 
remote_op(p);
```

El alias se produce en el ejemplo anterior porque la misma área de memoria está disponible en dos punteros diferentes en la función **p** y **p->** siguiente >anterior.

Tenga en cuenta **\[ que ignore \]** no se puede usar como atributo de tipo.

## <a name="examples"></a>Ejemplos

``` syntax
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    [ignore] struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE;
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos de matriz Sized-Pointer matriz](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**Matrices**](arrays-1.md)
</dt> <dt>

[Matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**En**](in.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Único**](unique.md)
</dt> </dl>

 

 