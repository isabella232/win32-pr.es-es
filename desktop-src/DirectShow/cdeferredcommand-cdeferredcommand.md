---
description: Método de constructor.
ms.assetid: 0b372fa2-78a9-4e38-813c-f18123716c6d
title: Constructor CDeferredCommand. CDeferredCommand (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.CDeferredCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e92a2ffc5129ee38fc5061b28ea7ffef49da0f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681197"
---
# <a name="cdeferredcommandcdeferredcommand-constructor"></a>Constructor CDeferredCommand. CDeferredCommand

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CDeferredCommand(
   CCmdQueue *pQ,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   LPUNKNOWN pUnkExecutor,
   REFTIME   time,
   GUID      *iid,
   long      dispidMethod,
   short     wFlags,
   long      cArgs,
   VARIANT   *pDispParams,
   VARIANT   *pvarResult,
   short     *puArgErr,
   BOOL      bStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pQ* 
</dt> <dd>

Puntero a un objeto que expone la interfaz [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) .

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntero a la interfaz **IUnknown** externa para la agregación.

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a un valor **HRESULT** devuelto.

</dd> <dt>

*pUnkExecutor* 
</dt> <dd>

Puntero al objeto que llevará a cabo este comando.

</dd> <dt>

*time* 
</dt> <dd>

Hora a la que se ejecutará el comando.

</dd> <dt>

*suscripto* 
</dt> <dd>

Puntero al identificador único global (**GUID**) de la interfaz que contiene el método.

</dd> <dt>

*dispidMethod* 
</dt> <dd>

Método de la interfaz que se va a llamar.

</dd> <dt>

*wFlags* 
</dt> <dd>

Contexto de la invocación.

</dd> <dt>

*cArgs* 
</dt> <dd>

Número de argumentos pasados.

</dd> <dt>

*pDispParams* 
</dt> <dd>

Puntero a una lista de tipos de variante de argumento.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Puntero a una lista de tipos Variant devuelta, si existe.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Puntero al último argumento de la lista de parámetros *pDispParams* con un error.

</dd> <dt>

*bStream* 
</dt> <dd>

Valor que indica si el tiempo de comando aplazado está en tiempo de secuencia (**true**) o en tiempo de presentación (**false**).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




