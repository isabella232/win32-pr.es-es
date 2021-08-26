---
description: El método RefreshDisplayType actualiza el formato de vídeo del objeto para que coincida con la pantalla especificada.
ms.assetid: cc2bdfeb-80f1-4fb6-859d-977d644a5e08
title: Método CImageDisplay.RefreshDisplayType (Winutil.h)
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
ms.openlocfilehash: d9184d5e8a0e0ad6c0242ec1dc4b7590f1bc0d39a0a9cd6a09b2676563a2796e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055475"
---
# <a name="cimagedisplayrefreshdisplaytype-method"></a>Método CImageDisplay.RefreshDisplayType

El `RefreshDisplayType` método actualiza el formato de vídeo del objeto para que coincida con la pantalla especificada.

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

Puntero a una cadena que contiene el nombre del dispositivo para mostrar, tal como lo devuelve la función **EnumDisplayDevices de** GDI. Para usar el dispositivo de pantalla principal, establezca este parámetro en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o E FAIL si no se realiza \_ correctamente.

## <a name="remarks"></a>Comentarios

Este método inicializa el miembro **m \_ Display** en un tipo de vídeo que se corresponde con el modo de presentación en el dispositivo especificado.

Llame a este método cada vez que se reciba un mensaje DISPLAYCHANGED de WM \_ o para especificar un dispositivo de visualización secundario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImageDisplay (clase)**](cimagedisplay.md)
</dt> </dl>

 

 




