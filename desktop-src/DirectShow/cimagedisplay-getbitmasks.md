---
description: El método GetBitMasks recupera las máscaras de color para un formato VIDEOINFO especificado.
ms.assetid: 72a9ba44-96de-4fff-a3fb-675d3dd080d8
title: Método CImageDisplay.GetBitMasks (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetBitMasks
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2defe5e80a0d7311adcd19dca67119019623993
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160198"
---
# <a name="cimagedisplaygetbitmasks-method"></a>Método CImageDisplay.GetBitMasks

El `GetBitMasks` método recupera las máscaras de color para un formato [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) especificado.

## <a name="syntax"></a>Sintaxis


```C++
const DWORD* GetBitMasks(
   const VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Puntero a la **estructura VIDEOINFO.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una matriz de tres **valores DWORD.**

## <a name="remarks"></a>Observaciones

Si el **miembro biCompression** es BI BITFIELDS, el método devuelve un puntero a las máscaras de color que se proporcionan en el \_ miembro **dwBitMasks.** Si el **miembro biCompression** es BI RGB, el método devuelve las máscaras de \_ color que corresponden a la profundidad de bits. Si se produce un error en el método (por ejemplo, la profundidad de bits es menor que 16), el método devuelve la matriz {0,0,0} .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CImageDisplay (clase)**](cimagedisplay.md)
</dt> </dl>

 

 




