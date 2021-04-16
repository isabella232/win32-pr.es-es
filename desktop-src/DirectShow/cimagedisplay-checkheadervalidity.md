---
description: El método CheckHeaderValidity valida una estructura BITMAPINFOHEADER. Este método solo es útil para los tipos RGB sin comprimir, no para los tipos comprimidos ni los tipos YUV.
ms.assetid: 24b547b6-b730-48b2-9a1b-6e77f9cb1ce1
title: Método CImageDisplay. CheckHeaderValidity (Winutil. h)
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
ms.openlocfilehash: 803e8cd1a70c68f3e20c320978e9a350bdf23bdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679086"
---
# <a name="cimagedisplaycheckheadervalidity-method"></a>CImageDisplay. CheckHeaderValidity, método

El `CheckHeaderValidity` método valida una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) . Este método solo es útil para los tipos RGB sin comprimir, no para los tipos comprimidos ni los tipos YUV.

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

Puntero a una estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) que contiene la estructura **BITMAPINFOHEADER** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si **BITMAPINFOHEADER** es válido o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Este método comprueba que las dimensiones de la imagen no son negativas; el tipo de compresión es de BI RGB o de campos de tipos de \_ BI \_ ; la profundidad de color y las máscaras de color son válidas, el miembro **biplaners** es igual a uno; y los miembros **bisize** y **biSizeImage** son correctos. También comprueba si hay errores comunes en las entradas de la paleta, si existen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




