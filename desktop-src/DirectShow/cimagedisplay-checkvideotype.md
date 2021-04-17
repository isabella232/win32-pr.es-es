---
description: El método CheckVideoType comprueba si un formato de videoinfo especificado es compatible con el formato de presentación.
ms.assetid: a8593c7d-bde0-4c44-b450-10c129dd0007
title: Método CImageDisplay. CheckVideoType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckVideoType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7db198270804053993352c4969b924fa7edc891f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661095"
---
# <a name="cimagedisplaycheckvideotype-method"></a>CImageDisplay. CheckVideoType, método

El `CheckVideoType` método comprueba si un formato de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) especificado es compatible con el formato de presentación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckVideoType(
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

Devuelve S \_ OK si el formato es compatible o E \_ INVALIDARG en caso contrario.

## <a name="remarks"></a>Observaciones

Este método devuelve S \_ OK si el tipo propuesto se puede mostrar fácilmente bajo la configuración de pantalla actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




