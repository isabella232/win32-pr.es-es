---
title: atributo void
description: El tipo de base void indica un procedimiento sin argumentos o un procedimiento que no devuelve un valor de resultado.
ms.assetid: a3eebfe7-bf43-4bab-b87b-9188a54ab9bf
keywords:
- atributo void de MIDL
topic_type:
- apiref
api_name:
- void
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b14a5ae4a2325f840d8a840cb0a1bc5283bb4a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105665761"
---
# <a name="void-attribute"></a>atributo void

El tipo de base **void** indica un procedimiento sin argumentos o un procedimiento que no devuelve un valor de resultado.

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

*nombre de función* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*lista de parámetros* 
</dt> <dd>

Especifica la lista de parámetros que se pasan a la función junto con los tipos de parámetros y atributos de parámetro asociados.

</dd> <dt>

*tipo de valor devuelto* 
</dt> <dd>

Especifica el nombre del tipo devuelto por la función.

</dd> <dt>

*context-Handle-type* 
</dt> <dd>

Especifica el nombre del tipo que toma el atributo de **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

El tipo de **puntero \* void**, que en C describe un puntero genérico que se puede convertir para representar cualquier tipo de puntero, está limitado en MIDL a su uso con la palabra clave de **\[ \_ identificador \] de contexto** .

## <a name="examples"></a>Ejemplos

``` syntax
void VoidFunc1(void); 
HRESULT VoidFunc2([in, out] short s1); 
typedef [context_handle] void * MY_CX_HNDL_TYPE; 
HRESULT InitHandle([out] MY_CX_HNDL_TYPE * ppCxHndl);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




