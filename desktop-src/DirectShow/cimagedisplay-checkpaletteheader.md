---
description: El método CheckPaletteHeader valida las entradas de la paleta en una estructura de videoinfo.
ms.assetid: bc18cbe6-0446-43a6-a50c-e587815b789d
title: Método CImageDisplay. CheckPaletteHeader (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckPaletteHeader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c4f401d2e75aeb35ffc19d26690fa04a769c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680925"
---
# <a name="cimagedisplaycheckpaletteheader-method"></a>CImageDisplay. CheckPaletteHeader, método

El `CheckPaletteHeader` método valida las entradas de la paleta en una estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

## <a name="syntax"></a>Sintaxis


```C++
BOOL CheckPaletteHeader(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInput* 
</dt> <dd>

Puntero a una estructura de **videoinfo** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si las entradas de la paleta son válidas o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Si el formato de la imagen no es de paleta, el método comprueba que **biClrUsed** sea igual a cero. De lo contrario, el método comprueba que el marcador de **bicompresión** es de BI \_ RGB; **biClrImportant** no es mayor que **biClrUsed**; y el número de entradas de la paleta no supera el máximo, dada la profundidad de color.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




