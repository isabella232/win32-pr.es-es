---
description: 'Constructor CDeferredCommand.CDeferredCommand: método constructor.'
ms.assetid: 0b372fa2-78a9-4e38-813c-f18123716c6d
title: Constructor CDeferredCommand.CDeferredCommand (Ctlutil.h)
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
ms.openlocfilehash: 9a10d8bba48902ed2d6fd66da8483cea1ba9aacc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119793"
---
# <a name="cdeferredcommandcdeferredcommand-constructor"></a>Constructor CDeferredCommand.CDeferredCommand

Método constructor.

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

*Pq* 
</dt> <dd>

Puntero a un objeto que expone la [**interfaz IQueueCommand.**](/windows/desktop/api/Control/nn-control-iqueuecommand)

</dd> <dt>

*Punk* 
</dt> <dd>

Puntero a la interfaz **IUnknown externa** para la agregación.

</dd> <dt>

*Phr* 
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

*Iid* 
</dt> <dd>

Puntero al identificador único global **(GUID)** de la interfaz que contiene el método .

</dd> <dt>

*dispidMethod* 
</dt> <dd>

Método en la interfaz a la que se llamará.

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

Puntero a una lista de tipo variante devuelta, si la hay.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Puntero al último argumento de la lista *de parámetros pDispParams* con un error.

</dd> <dt>

*bStream* 
</dt> <dd>

Valor que indica si el tiempo de comando diferido está en tiempo de secuencia (**TRUE**) o tiempo de presentación (**FALSE**).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDeferredCommand (clase)**](cdeferredcommand.md)
</dt> </dl>

 

 




