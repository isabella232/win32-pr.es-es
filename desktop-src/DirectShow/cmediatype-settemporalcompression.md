---
description: El método SetComposiciónCompression especifica si las muestras se comprimen mediante compresión temporal (interframe).
ms.assetid: cdd181ee-d1e9-48b0-96f6-e76db9f3f933
title: Método CMediaType.SetComposiciónCompression (Mtype.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362494"
---
# <a name="cmediatypesettemporalcompression-method"></a>Método CMediaType.SetComposiciónCompression

El `SetTemporalCompression` método especifica si las muestras se comprimen mediante compresión temporal (interframe).

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

Valor booleano que especifica si la secuencia usa la compresión temporal. Si la secuencia usa la compresión temporal, establezca el valor en **TRUE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método establece el **miembro bComposiciónCompression.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 




