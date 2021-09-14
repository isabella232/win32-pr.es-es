---
description: La interfaz IAMTimelineComp inserta o recupera pistas virtuales en una composición en DirectShow Editing Services (DES). Una composición es una colección de capas que actúa como una sola pista compuesta.
ms.assetid: b0a47303-9e3c-4b78-ac90-c5d8fce2b727
title: Interfaz IAMTimelineComp (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 645abbb9c5f61fcfd04e433c3cfc61b926ed403d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892140"
---
# <a name="iamtimelinecomp-interface"></a>Interfaz IAMTimelineComp

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La **interfaz IAMTimelineComp** inserta o recupera pistas virtuales en una composición [en DirectShow Editing Services](directshow-editing-services.md) (DES).

Una composición es una colección de capas que actúa como una sola pista *compuesta.* Por ejemplo, una composición que contiene dos pistas con una transición entre ellas actúa como una sola pista con la transición precompilada. Una composición debe contener medios de un solo tipo (como audio o vídeo), pero esta limitación no se aplica. Una *pista virtual* es cualquier objeto que puede residir en una composición, incluidas las pistas y otras composiciones.

Los nodos superiores de la escala de tiempo son *los grupos*. Los grupos implementan la `IAMTimelineComp` interfaz y la interfaz [**IAMTimelineGroup.**](iamtimelinegroup.md)

Para crear un objeto de composición, llame a [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) con el valor TIMELINE \_ MAJOR TYPE \_ \_ COMPOSITE. Puede consultar el puntero [**IAMTimelineObj**](iamtimelineobj.md) devuelto para la `IAMTimelineComp` interfaz . Para obtener más información, vea [Modelo de escala de tiempo](the-timeline-model.md) y Construcción de una escala de [tiempo.](constructing-a-timeline.md)

## <a name="members"></a>Members

La **interfaz IAMTimelineComp** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineComp también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IAMTimelineComp** tiene estos métodos.



| Método                                                                       | Descripción                                                                                                                                               |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCountOfType**](iamtimelinecomp-getcountoftype.md)                     | Recupera el número de objetos de un tipo determinado contenidos en esta composición y todas sus pistas virtuales de forma recursiva.<br/>                      |
| [**GetNextVTrack**](iamtimelinecomp-getnextvtrack.md)                       | Recupera la siguiente pista virtual después de una pista virtual especificada.<br/>                                                                              |
| [**GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md)   | Realiza una ordenación en profundidad de las pistas virtuales contenidas en esta composición y recupera la enésima pista virtual de esa ordenación.<br/> |
| [**GetRecursiveLayerOfTypeI**](iamtimelinecomp-getrecursivelayeroftypei.md) | No compatible.<br/>                                                                                                                                 |
| [**GetVTrack**](iamtimelinecomp-getvtrack.md)                               | Recupera la pista virtual con la prioridad especificada.<br/>                                                                                         |
| [**VTrackGetCount**](iamtimelinecomp-vtrackgetcount.md)                     | Recupera el número de pistas virtuales contenidas en la composición.<br/>                                                                           |
| [**VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md)                   | Inserta una pista virtual en la composición con la prioridad especificada.<br/>                                                                        |
| [**VTrackSwapPriorities**](iamtimelinecomp-vtrackswappriorities.md)         | Cambia los niveles de prioridad de dos pistas.<br/>                                                                                                    |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
