---
description: La interfaz IAMTimelineVirtualTrack proporciona métodos para trabajar con pistas virtuales en DirectShow Editing Services (DES). Las composiciones y pistas admiten esta interfaz.
ms.assetid: 69d1d2ea-d33f-406d-a9ca-ddfb890bed34
title: Interfaz IAMTimelineVirtualTrack (Qedit.h)
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
ms.openlocfilehash: f9eba273793e97c5fb92fdabb365eb2402fc6feb6fbc571f1ec1ef1a0a4b3692
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982775"
---
# <a name="iamtimelinevirtualtrack-interface"></a>Interfaz IAMTimelineVirtualTrack

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IAMTimelineVirtualTrack` interfaz proporciona métodos para trabajar con pistas virtuales [en DirectShow Editing Services](directshow-editing-services.md) (DES). Las composiciones y pistas admiten esta interfaz.

## <a name="members"></a>Miembros

La **interfaz IAMTimelineVirtualTrack** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineVirtualTrack** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IAMTimelineVirtualTrack** tiene estos métodos.



| Método                                                               | Descripción                                       |
|:---------------------------------------------------------------------|:--------------------------------------------------|
| [**SetTrackDirty**](iamtimelinevirtualtrack-settrackdirty.md)       | No compatible.<br/>                         |
| [**TrackGetPriority**](iamtimelinevirtualtrack-trackgetpriority.md) | Recupera el nivel de prioridad del objeto.<br/> |



 

## <a name="remarks"></a>Comentarios

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
