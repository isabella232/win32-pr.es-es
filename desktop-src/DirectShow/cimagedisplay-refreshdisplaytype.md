---
description: El método RefreshDisplayType actualiza el formato de vídeo del objeto para que coincida con la presentación especificada.
ms.assetid: cc2bdfeb-80f1-4fb6-859d-977d644a5e08
title: Método CImageDisplay. RefreshDisplayType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.RefreshDisplayType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f8010dcfe490363903ff455bedb61254b69b825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680460"
---
# <a name="cimagedisplayrefreshdisplaytype-method"></a>CImageDisplay. RefreshDisplayType, método

El `RefreshDisplayType` método actualiza el formato de vídeo del objeto para que coincida con la presentación especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RefreshDisplayType(
   LPSTR szDeviceName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szDeviceName* 
</dt> <dd>

Puntero a una cadena que contiene el nombre del dispositivo de pantalla, devuelto por la función **EnumDisplayDevices** de GDI. Para usar el dispositivo de pantalla principal, establezca este parámetro en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve \_ si es correcto, o E \_ produce un error si no se realiza correctamente.

## <a name="remarks"></a>Observaciones

Este método inicializa el miembro **de \_ visualización m** en un tipo de vídeo que corresponde al modo de presentación en el dispositivo especificado.

Llame a este método cada vez que \_ se reciba un mensaje de DISPLAYCHANGED de WM, o para especificar un dispositivo de pantalla secundario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




