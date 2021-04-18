---
description: El método ModifyStopTime establece la hora de detención, relativa a la escala de tiempo.
ms.assetid: 0d9b6cf7-d029-4c35-9045-82cbeff1e3ae
title: 'IAMTimelineSrc:: ModifyStopTime (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5e0f3ac58df4e74926d2163705261ffad4551e69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681072"
---
# <a name="iamtimelinesrcmodifystoptime-method"></a>IAMTimelineSrc:: ModifyStopTime (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `ModifyStopTime` método establece la hora de detención, relativa a la escala de tiempo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ModifyStopTime(
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Detención* 
</dt> <dd>

Nueva hora de detención, en unidades de 100-nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ INVALIDARG si la hora especificada no es válida.

## <a name="remarks"></a>Observaciones

Este método equivale a llamar a [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) con la hora de inicio original y una nueva hora de detención.

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

[**Interfaz IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




