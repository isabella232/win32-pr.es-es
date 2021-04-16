---
description: El nuevo método inicializa un comando que se va a ejecutar y devuelve un nuevo objeto CDeferredCommand.
ms.assetid: bdd80747-a15b-422a-b742-ebfa4076bdf7
title: Método CCmdQueue. New (Winutil. h)
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
ms.openlocfilehash: 58c3aee63005010b9ed7366cfb63a69fcc7348b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678958"
---
# <a name="ccmdqueuenew-method"></a>CCmdQueue. New (método)

El `New` método inicializa un comando que se va a ejecutar y devuelve un nuevo objeto [**CDeferredCommand**](cdeferredcommand.md) .

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

Dirección de un puntero a un objeto [**CDeferredCommand**](cdeferredcommand.md) por el que una aplicación puede cancelar el comando, establecer un nuevo tiempo de presentación para el mismo o recuperar la información de estimación.

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntero al objeto que ejecutará el comando.

</dd> <dt>

*time* 
</dt> <dd>

Hora a la que se va a ejecutar el comando o comandos en cola.

</dd> <dt>

*suscripto* 
</dt> <dd>

Puntero al identificador único global (**GUID**) de la interfaz a la que se va a llamar.

</dd> <dt>

*dispidMethod* 
</dt> <dd>

Método en la interfaz a la que se va a llamar.

</dd> <dt>

*wFlags* 
</dt> <dd>

Marcas que describen el contexto de la llamada. Este parámetro admite las mismas marcas que el método **IDispatch:: Invoke** .

</dd> <dt>

*cArgs* 
</dt> <dd>

Número de argumentos pasados.

</dd> <dt>

*pDispParams* 
</dt> <dd>

Puntero a la lista de tipos Variant asociados a los parámetros de envío.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Puntero a la lista donde se van a devolver los resultados, si los hay.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Puntero al índice de la lista de parámetros *pDispParams* donde se produjo el último error.

</dd> <dt>

*bStream* 
</dt> <dd>

Valor que indica si el parámetro de *hora* es un valor de tiempo de secuencia (**true**) o un valor de tiempo de presentación (**false**).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto si se realiza correctamente. Devuelve E \_ OUTOFMEMORY si *ppCmd* vuelve de crear el nuevo objeto [**CDeferredCommand**](cdeferredcommand.md) con un valor **null**. De lo contrario, devuelve un **valor HRESULT** que indica un error al intentar crear un nuevo objeto **CDeferredCommand** . Si se produce un error, no se ha puesto en cola ningún objeto.

## <a name="remarks"></a>Observaciones

El nuevo objeto [**CDeferredCommand**](cdeferredcommand.md) se inicializará con los parámetros y se agregará a la cola durante la construcción. Este método es similar al método **IDispatch:: Invoke** .

Los valores para el parámetro *wFlags* son los siguientes:



| Value                    | Descripción                                                                                                                                                          |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DISPATCH ( \_ método)         | El miembro se está ejecutando como un método. Si una propiedad tiene el mismo nombre, se pueden establecer tanto esta marca como la de envío \_ PropertyGet (.                                       |
| ENVIAR \_ PropertyGet (    | El miembro se recupera como una propiedad o miembro de datos.                                                                                                          |
| ENVIAR \_ PROPERTYPUT    | El miembro se está cambiando como una propiedad o un miembro de datos.                                                                                                            |
| ENVIAR \_ PROPERTYPUTREF | El miembro se está cambiando a través de una asignación de referencia, en lugar de una asignación de valores. Este valor solo es válido cuando la propiedad acepta una referencia a un objeto. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




