---
description: El método CheckBitFields valida las máscaras de color en una estructura de videoinfo.
ms.assetid: b03455aa-8d90-4fab-999d-7408d8417021
title: Método CImageDisplay. CheckBitFields (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckBitFields
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade581dad5e53c2454df52e387653e44d6d4ad2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660226"
---
# <a name="cimagedisplaycheckbitfields-method"></a>CImageDisplay. CheckBitFields, método

El `CheckBitFields` método valida las máscaras de color en una estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

## <a name="syntax"></a>Sintaxis


```C++
BOOL CheckBitFields(
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

Devuelve **true** si las máscaras de color son válidas o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Este método comprueba que la máscara de color para cada componente de color está comprendida entre uno y ocho bits de longitud y que cada máscara de color es una secuencia contigua de bits. Llame a este método solo cuando el miembro **bicompression** esté establecido en \_ campos de campos de BI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




