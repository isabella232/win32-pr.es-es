---
title: omitir atributo
description: El atributo \ ignore \ designa que no se transmite un puntero contenido en una estructura o Unión y el objeto indicado por el puntero. El atributo \ ignore \ está restringido a los miembros de puntero de estructuras o uniones.
ms.assetid: 9c2fc71a-4fac-4a59-95f5-2121067b326f
keywords:
- omitir el atributo MIDL
topic_type:
- apiref
api_name:
- ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e82b9525dd6de316087db8fdfd55181118d3adc6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904539"
---
# <a name="ignore-attribute"></a>omitir atributo

El atributo **\[ Ignore \]** designa que no se transmite un puntero contenido en una estructura o Unión y el objeto indicado por el puntero. El atributo **\[ Ignore \]** está restringido a los miembros de puntero de estructuras o uniones.

``` syntax
[ignore] pointer-member-type pointer-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo de miembro de puntero* 
</dt> <dd>

Especifica el tipo del miembro de puntero de la estructura o Unión.

</dd> <dt>

*puntero: nombre* 
</dt> <dd>

Especifica el nombre del miembro de puntero que se va a omitir durante el cálculo de referencias.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El valor de un miembro de estructura con el atributo **\[ Ignore \]** no está definido en el destino. Un **\[** parámetro [**in**](in.md) **\]** no está definido en el equipo remoto. Un **\[** parámetro [**out**](out-idl.md) **\]** no está definido en el equipo local.

El atributo **\[ Ignore \]** permite evitar la transmisión de datos. Esto resulta útil en situaciones como una lista de vínculos dobles. En el ejemplo siguiente se incluye una lista de vínculos dobles que presenta los alias de datos:

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

El alias se produce en el ejemplo anterior porque el mismo área de memoria está disponible en dos punteros diferentes en la función **p** y **p->siguiente->anterior**.

Tenga en cuenta que no se puede usar **\[ Ignore \]** como atributo de tipo.

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

[Atributos array y Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**matrices**](arrays-1.md)
</dt> <dt>

[Matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**de**](in.md)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**espeficarse**](unique.md)
</dt> </dl>

 

 