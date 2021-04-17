---
description: Método de constructor.
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: Constructor CAMThread. CAMThread (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abaac0c3b0330cd41db7ecd21f894733de10a1b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661149"
---
# <a name="camthreadcamthread-constructor"></a>Constructor CAMThread. CAMThread

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phr* 
</dt> <dd>

Puntero a un valor **HRESULT** . Si se produce un error en el constructor, este parámetro recibe un código de error. Si esto ocurre, el objeto no tiene un estado válido.

Para mantener la compatibilidad con versiones anteriores de strmbase. lib, este parámetro tiene como valor predeterminado **null**. Sin embargo, se prefiere pasar un valor distinto de **null** para que el autor de la llamada pueda comprobar el estado del objeto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El método de constructor no crea el subproceso. Para crear el subproceso, llame al método [**CAMThread:: Create**](camthread-create.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMThread**](camthread.md)
</dt> </dl>

 

 




