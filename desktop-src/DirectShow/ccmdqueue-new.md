---
description: El método New inicializa un comando que se va a ejecutar y devuelve un nuevo objeto CDeferredCommand.
ms.assetid: bdd80747-a15b-422a-b742-ebfa4076bdf7
title: Método CCmdQueue.New (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.New
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b6ad22b67df863e699649f22f513a98ca1306751a1d449a683f306c9cc2938
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910395"
---
# <a name="ccmdqueuenew-method"></a>Método CCmdQueue.New

El `New` método inicializa un comando que se va a ejecutar y devuelve un nuevo objeto [**CDeferredCommand.**](cdeferredcommand.md)

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT New(
   CDeferredCommand **ppCmd,
   LPUNKNOWN        pUnk,
   REFTIME          time,
   GUID             *iid,
   long             dispidMethod,
   short            wFlags,
   long             cArgs,
   VARIANT          *pDispParams,
   VARIANT          *pvarResult,
   short            *puArgErr,
   BOOL             bStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppCmd* 
</dt> <dd>

Dirección de un puntero a un objeto [**CDeferredCommand**](cdeferredcommand.md) por el que una aplicación puede cancelar el comando, establecer un nuevo tiempo de presentación para él o recuperar información de estimación.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntero al objeto que ejecutará el comando.

</dd> <dt>

*time* 
</dt> <dd>

Hora a la que se va a ejecutar el comando o los comandos en cola.

</dd> <dt>

*Iid* 
</dt> <dd>

Puntero al identificador único global **(GUID)** de la interfaz a la que se llamará.

</dd> <dt>

*dispidMethod* 
</dt> <dd>

Método en la interfaz a la que se va a llamar.

</dd> <dt>

*wFlags* 
</dt> <dd>

Marcas que describen el contexto de la llamada. Este parámetro admite las mismas marcas que el **método IDispatch::Invoke.**

</dd> <dt>

*cArgs* 
</dt> <dd>

Número de argumentos pasados.

</dd> <dt>

*pDispParams* 
</dt> <dd>

Puntero a la lista de tipos variantes asociados a los parámetros de distribución.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Puntero a la lista donde se van a devolver los resultados, si los hay.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Puntero al índice dentro de la lista *de parámetros pDispParams* donde se produjo el último error.

</dd> <dt>

*bStream* 
</dt> <dd>

Valor que indica si el *parámetro time* es un valor de tiempo de secuencia **(TRUE)** o un valor de tiempo de presentación **(FALSE).**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente. Devuelve E \_ OUTOFMEMORY si *ppCmd* devuelve al crear el nuevo [**objeto CDeferredCommand**](cdeferredcommand.md) con un valor **null.** De lo contrario, **devuelve un valor HRESULT** que indica un error al intentar crear un nuevo **objeto CDeferredCommand.** Si se produce un error, no se ha puesto en cola ningún objeto.

## <a name="remarks"></a>Comentarios

El nuevo [**objeto CDeferredCommand**](cdeferredcommand.md) se inicializará con los parámetros y se agregará a la cola durante la construcción. Este método es similar al **método IDispatch::Invoke.**

Entre los valores del *parámetro wFlags* se incluyen los siguientes:



| Value                    | Descripción                                                                                                                                                          |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DISPATCH \_ (MÉTODO)         | El miembro se ejecuta como un método. Si una propiedad tiene el mismo nombre, se pueden establecer tanto esta como la marca DISPATCH \_ PROPERTYGET.                                       |
| DISPATCH \_ PROPERTYGET    | El miembro se recupera como una propiedad o un miembro de datos.                                                                                                          |
| DISPATCH \_ PROPERTYPUT    | El miembro se está cambiando como una propiedad o un miembro de datos.                                                                                                            |
| DISPATCH \_ PROPERTYPUTREF | El miembro se cambia a través de una asignación de referencia, en lugar de una asignación de valor. Este valor solo es válido cuando la propiedad acepta una referencia a un objeto . |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CCmdQueue (clase)**](ccmdqueue.md)
</dt> </dl>

 

 




