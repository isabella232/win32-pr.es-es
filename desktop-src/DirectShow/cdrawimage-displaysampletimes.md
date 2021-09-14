---
description: El método DisplaySampleTimes dibuja las marcas de tiempo de un ejemplo multimedia sobre la imagen de vídeo.
ms.assetid: 3741dc74-5311-4cb1-9e6b-4a8bf6113477
title: Método CDrawImage.DisplaySampleTimes (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DisplaySampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9988aaedf9a1c01c83412cdbe9e00533556c9b15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061302"
---
# <a name="cdrawimagedisplaysampletimes-method"></a>Método CDrawImage.DisplaySampleTimes

El `DisplaySampleTimes` método dibuja las marcas de tiempo de un ejemplo multimedia sobre la imagen de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
void DisplaySampleTimes(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSample* 
</dt> <dd>

Puntero a la [**interfaz IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Solo se llama a este método en compilaciones de depuración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDrawImage (clase)**](cdrawimage.md)
</dt> </dl>

 

 




