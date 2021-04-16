---
description: 'El método ZeroBetween2 quita todo de la pista entre las horas especificadas. Este método es equivalente a IAMTimelineTrack:: ZeroBetween, pero toma valores REFTIME.'
ms.assetid: 56b9be30-cc3f-4843-bf35-910498242d71
title: 'IAMTimelineTrack:: ZeroBetween2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 27e3ab5cc2a631cb54c926824c2f3410413cd981
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690110"
---
# <a name="iamtimelinetrackzerobetween2-method"></a>IAMTimelineTrack:: ZeroBetween2 (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `ZeroBetween2` método quita todo de la pista entre las horas especificadas. Este método es equivalente a [**IAMTimelineTrack:: ZeroBetween**](iamtimelinetrack-zerobetween.md), pero toma valores [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ZeroBetween2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rtStart* 
</dt> <dd>

Comienzo del intervalo que se va a borrar, en segundos.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Final del intervalo que se va a borrar, en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                             | Descripción                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | El intervalo de tiempo está por encima de todo en la pista.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Correcto.<br/>                                             |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IAMTimelineTrack**](iamtimelinetrack.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




