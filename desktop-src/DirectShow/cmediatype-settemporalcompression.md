---
description: El método SetTemporalCompression especifica si los ejemplos se comprimen mediante la compresión temporal (interframe).
ms.assetid: cdd181ee-d1e9-48b0-96f6-e76db9f3f933
title: Método CMediaType. SetTemporalCompression (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetTemporalCompression
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0aba07375c5b5c760c432de704562efb2bea148
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680284"
---
# <a name="cmediatypesettemporalcompression-method"></a>CMediaType. SetTemporalCompression, método

El `SetTemporalCompression` método especifica si los ejemplos se comprimen mediante la compresión temporal (interframe).

## <a name="syntax"></a>Sintaxis


```C++
void SetTemporalCompression(
   BOOL bCompressed
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bCompressed* 
</dt> <dd>

Valor booleano que especifica si la secuencia utiliza la compresión temporal. Si la secuencia utiliza la compresión temporal, establezca el valor en **true**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método establece el miembro **bTemporalCompression** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaType**](cmediatype.md)
</dt> </dl>

 

 




