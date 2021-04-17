---
description: La interfaz IAMTimelineVirtualTrack proporciona métodos para trabajar con pistas virtuales en los servicios de edición de DirectShow (DES). Las composiciones y las pistas admiten esta interfaz.
ms.assetid: 69d1d2ea-d33f-406d-a9ca-ddfb890bed34
title: Interfaz IAMTimelineVirtualTrack (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2295f1c336270818242f0d992a369e6a66f9237a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690321"
---
# <a name="iamtimelinevirtualtrack-interface"></a>Interfaz IAMTimelineVirtualTrack

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IAMTimelineVirtualTrack` interfaz proporciona métodos para trabajar con pistas virtuales en los [servicios de edición de DirectShow](directshow-editing-services.md) (des). Las composiciones y las pistas admiten esta interfaz.

## <a name="members"></a>Miembros

La interfaz **IAMTimelineVirtualTrack** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineVirtualTrack** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IAMTimelineVirtualTrack** tiene estos métodos.



| Método                                                               | Descripción                                       |
|:---------------------------------------------------------------------|:--------------------------------------------------|
| [**SetTrackDirty**](iamtimelinevirtualtrack-settrackdirty.md)       | No se admite.<br/>                         |
| [**TrackGetPriority**](iamtimelinevirtualtrack-trackgetpriority.md) | Recupera el nivel de prioridad del objeto.<br/> |



 

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



 

 
