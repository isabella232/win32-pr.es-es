---
description: 'Constructor CAMThread.CAMThread: método constructor.'
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: Constructor CAMThread.CAMThread (Wxutil.h)
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
ms.openlocfilehash: 0c4b9c5f80e131ce089b6a2da924e9cca41a84f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160268"
---
# <a name="camthreadcamthread-constructor"></a>Constructor CAMThread.CAMThread

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Phr* 
</dt> <dd>

Puntero a un **valor HRESULT.** Si se produce un error en el constructor, este parámetro recibe un código de error. Si esto ocurre, el objeto no está en un estado válido.

Para la compatibilidad con versiones anteriores de strmbase.lib, este parámetro tiene como valor predeterminado **NULL**. Sin embargo, se prefiere pasar un valor distinto de **NULL,** para que el autor de la llamada pueda comprobar el estado del objeto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El método constructor no crea el subproceso. Para crear el subproceso, llame al [**método CAMThread::Create.**](camthread-create.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




