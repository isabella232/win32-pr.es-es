---
description: 'El método ModifyStopTime2 establece la hora de detención. Este método es equivalente a IAMTimelineSrc:: ModifyStopTime, pero toma un valor REFTIME.'
ms.assetid: 8bebda47-3e52-42a2-870c-acc14561fa25
title: 'IAMTimelineSrc:: ModifyStopTime2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 42ca3c9c1f8fa47abc7a9c21a44458540007939f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690938"
---
# <a name="iamtimelinesrcmodifystoptime2-method"></a>IAMTimelineSrc:: ModifyStopTime2 (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `ModifyStopTime2` método establece la hora de detención. Este método es equivalente a [**IAMTimelineSrc:: ModifyStopTime**](iamtimelinesrc-modifystoptime.md), pero toma un valor [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ModifyStopTime2(
   REFTIME Stop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Detención* 
</dt> <dd>

Nuevo tiempo de detención, en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve \_ si es correcto, o E \_ INVALIDARG si la hora especificada no es válida.

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

[**Interfaz IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




