---
description: El método SetDIBData especifica información sobre el mapa de bits independiente del dispositivo GDI (DIB) que este objeto está administrando. Llame a este método para inicializar el objeto CImageSample.
ms.assetid: 850fa16b-d4b9-4fe6-b202-7b54c49a4589
title: Método CImageSample.SetDIBData (Winutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273068"
---
# <a name="cimagesamplesetdibdata-method"></a>Método CImageSample.SetDIBData

El método especifica información sobre el mapa de bits independiente del dispositivo `SetDIBData` (DIB) GDI que este objeto está administrando. Llame a este método para inicializar el **objeto CImageSample.**

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

Puntero a una [**estructura DIBDATA.**](dibdata.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CImageSample (clase)**](cimagesample.md)
</dt> </dl>

 

 




