---
description: El método CheckBitFields valida las máscaras de color en una estructura VIDEOINFO.
ms.assetid: b03455aa-8d90-4fab-999d-7408d8417021
title: Método CImageDisplay.CheckBitFields (Winutil.h)
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
ms.openlocfilehash: 44e60b6693dde202cd458cd09495dce9e4bea52ed96a468a8d3dcb6b2370eac4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074179"
---
# <a name="cimagedisplaycheckbitfields-method"></a>Método CImageDisplay.CheckBitFields

El `CheckBitFields` método valida las máscaras de color en una [**estructura VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)

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

Puntero a una **estructura VIDEOINFO.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si las máscaras de color son válidas o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

Este método comprueba que la máscara de color para cada componente de color tiene entre uno y ocho bits de longitud, y que cada máscara de color es una secuencia contigua de bits. Llame a este método solo cuando **el miembro biCompression** esté establecido en BI \_ BITFIELDS.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImageDisplay (clase)**](cimagedisplay.md)
</dt> </dl>

 

 




