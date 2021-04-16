---
description: El método SetDIBData especifica información sobre el mapa de bits independiente del dispositivo GDI (DIB) que este objeto administra. Llame a este método para inicializar el objeto CImageSample.
ms.assetid: 850fa16b-d4b9-4fe6-b202-7b54c49a4589
title: Método CImageSample. SetDIBData (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.SetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 418263da0416b325b1b080713dd6289f3bcc688e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670487"
---
# <a name="cimagesamplesetdibdata-method"></a>CImageSample. SetDIBData, método

El `SetDIBData` método especifica información sobre el mapa de bits independiente del dispositivo GDI (DIB) que este objeto administra. Llame a este método para inicializar el objeto **CImageSample** .

## <a name="syntax"></a>Sintaxis


```C++
void SetDIBData(
   DIBDATA *pDibData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDibData* 
</dt> <dd>

Puntero a una estructura [**DIBDATA**](dibdata.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImageSample**](cimagesample.md)
</dt> </dl>

 

 




