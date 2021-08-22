---
description: El método GetDisplayFormat recupera un formato de vídeo que describe el modo de presentación actual.
ms.assetid: 98134704-0453-4090-94de-d92cdf324538
title: Método CImageDisplay.GetDisplayFormat (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetDisplayFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8841e95f4097d043e7ef01abdb067c248f43b9295a8c8466ba50f07d23bd7dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074149"
---
# <a name="cimagedisplaygetdisplayformat-method"></a>Método CImageDisplay.GetDisplayFormat

El `GetDisplayFormat` método recupera un formato de vídeo que describe el modo de presentación actual.

## <a name="syntax"></a>Sintaxis


```C++
const VIDEOINFO* GetDisplayFormat();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a una [**estructura VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImageDisplay (clase)**](cimagedisplay.md)
</dt> </dl>

 

 




