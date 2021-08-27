---
description: El método CheckVideoType comprueba si un formato VIDEOINFO especificado es compatible con el formato de presentación.
ms.assetid: a8593c7d-bde0-4c44-b450-10c129dd0007
title: Método CImageDisplay.CheckVideoType (Winutil.h)
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
ms.openlocfilehash: de6389e22868fe529b5038fe6be1403748dd5a01d22a242c41f9e6c6b8f86808
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108495"
---
# <a name="cimagedisplaycheckvideotype-method"></a>Método CImageDisplay.CheckVideoType

El `CheckVideoType` método comprueba si un formato [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) especificado es compatible con el formato de presentación.

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

Puntero a una **estructura VIDEOINFO.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el formato es compatible o E \_ INVALIDARG en caso contrario.

## <a name="remarks"></a>Comentarios

Este método devuelve S OK si el tipo propuesto \_ se puede mostrar fácilmente en la configuración de presentación actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImageDisplay (clase)**](cimagedisplay.md)
</dt> </dl>

 

 




