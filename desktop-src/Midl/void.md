---
title: void (atributo)
description: El tipo base void indica un procedimiento sin argumentos o un procedimiento que no devuelve un valor de resultado.
ms.assetid: a3eebfe7-bf43-4bab-b87b-9188a54ab9bf
keywords:
- atributo void MIDL
topic_type:
- apiref
api_name:
- void
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ad758ba334114e13493e7b082f45f37dc6e68efba16dc3a55f14fa57a772d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382441"
---
# <a name="void-attribute"></a>void (atributo)

El tipo base **void** indica un procedimiento sin argumentos o un procedimiento que no devuelve un valor de resultado.

``` syntax
void function-name(parameter-list);

return-type function-name(void);

typedef [context_handle] void * context-handle-type;

return-type function-name(
    [context_handle] void * * context-handle-type
    , ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*parameter-list* 
</dt> <dd>

Especifica la lista de parámetros pasados a la función junto con los tipos de parámetros asociados y los atributos de parámetro.

</dd> <dt>

*return-type* 
</dt> <dd>

Especifica el nombre del tipo devuelto por la función.

</dd> <dt>

*context-handle-type* 
</dt> <dd>

Especifica el nombre del tipo que toma el atributo **\[** [**de identificador \_ de**](context-handle.md) **\]** contexto.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El tipo de puntero void _, que en C describe un puntero genérico que se puede convertir para representar cualquier tipo de puntero, está limitado en MIDL a su uso con la palabra clave **\* *_* \[ context \_ handle. \]**

## <a name="examples"></a>Ejemplos

``` syntax
void VoidFunc1(void); 
HRESULT VoidFunc2([in, out] short s1); 
typedef [context_handle] void * MY_CX_HNDL_TYPE; 
HRESULT InitHandle([out] MY_CX_HNDL_TYPE * ppCxHndl);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**identificador de \_ contexto**](context-handle.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




