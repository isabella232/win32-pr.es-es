---
description: El método CheckHeaderValidity valida una estructura BITMAPINFOHEADER. Este método solo es útil para los tipos RGB sin comprimir, no para los tipos comprimidos o los tipos YUV.
ms.assetid: 24b547b6-b730-48b2-9a1b-6e77f9cb1ce1
title: Método CImageDisplay.CheckHeaderValidity (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckHeaderValidity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25c8ce12f7e383e04942184e3897d0ddc52700a1a621844719d94f54f60203ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652365"
---
# <a name="cimagedisplaycheckheadervalidity-method"></a>Método CImageDisplay.CheckHeaderValidity

El `CheckHeaderValidity` método valida una [**estructura BITMAPINFOHEADER.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) Este método solo es útil para los tipos RGB sin comprimir, no para los tipos comprimidos o los tipos YUV.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CheckHeaderValidity(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInput* 
</dt> <dd>

Puntero a una [**estructura VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) que contiene la **estructura BITMAPINFOHEADER.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** **BITMAPINFOHEADER** es válido o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

Este método comprueba que las dimensiones de la imagen no son negativas; El tipo de compresión es BI RGB o BI BITFIELDS; la profundidad de color y las máscaras de color son válidas; el miembro biPlanes es igual a uno y los miembros \_ \_ **biSize** y **biSizeImage** son correctos.  También comprueba si hay errores comunes en las entradas de la paleta, si las hay.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImageDisplay (clase)**](cimagedisplay.md)
</dt> </dl>

 

 




