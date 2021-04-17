---
description: El método TrackGetPriority recupera el nivel de prioridad del objeto.
ms.assetid: f9a138e8-e9ad-4703-bdcc-c64aea4fbad0
title: 'IAMTimelineVirtualTrack:: TrackGetPriority (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack.TrackGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 08b43fa34848e5dac41d22281c08d25ee9065831
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690858"
---
# <a name="iamtimelinevirtualtracktrackgetpriority-method"></a>IAMTimelineVirtualTrack:: TrackGetPriority (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `TrackGetPriority` método recupera el nivel de prioridad del objeto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT TrackGetPriority(
   long *pPriority
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPriority* 
</dt> <dd>

Puntero a una variable que recibe el nivel de prioridad. Si el objeto no forma parte de una escala de tiempo, el valor se establece en – 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

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

[**Interfaz IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




