---
description: La interfaz IAMTimelineComp inserta o recupera pistas virtuales en una composición en los servicios de edición de DirectShow (DES). Una composición es una colección de capas que actúa como una única pista compuesta.
ms.assetid: b0a47303-9e3c-4b78-ac90-c5d8fce2b727
title: Interfaz IAMTimelineComp (QEDIT. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681260"
---
# <a name="iamtimelinecomp-interface"></a>Interfaz IAMTimelineComp

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La interfaz **IAMTimelineComp** inserta o recupera pistas virtuales en una composición en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).

Una composición es una colección de capas que actúa como una única *pista* compuesta. Por ejemplo, una composición que contiene dos pistas con una transición entre ellas actúa como una sola pista con la transición precompuesta. Una composición debe contener medios de un solo tipo (como audio o vídeo), pero esta limitación no se aplica. Una *pista virtual* es cualquier objeto que puede residir en una composición, incluidas las pistas y otras composiciones.

Los nodos de nivel superior de la escala de tiempo son *grupos*. Los grupos implementan la `IAMTimelineComp` interfaz y la interfaz [**IAMTimelineGroup**](iamtimelinegroup.md) .

Para crear un objeto de composición, llame a [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con el tipo principal de la escala de tiempo de valor \_ \_ \_ compuesto. Puede consultar el puntero [**IAMTimelineObj**](iamtimelineobj.md) devuelto para la `IAMTimelineComp` interfaz. Para obtener más información, vea [el modelo Timeline](the-timeline-model.md) y [crear una escala de tiempo](constructing-a-timeline.md).

## <a name="members"></a>Miembros

La interfaz **IAMTimelineComp** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineComp** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IAMTimelineComp** tiene estos métodos.



| Método                                                                       | Descripción                                                                                                                                               |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCountOfType**](iamtimelinecomp-getcountoftype.md)                     | Recupera el número de objetos de un tipo determinado contenidos en esta composición y todas sus pistas virtuales de forma recursiva.<br/>                      |
| [**GetNextVTrack**](iamtimelinecomp-getnextvtrack.md)                       | Recupera la siguiente pista virtual después de una pista virtual especificada.<br/>                                                                              |
| [**GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md)   | Realiza una ordenación con prioridad a la profundidad de las pistas virtuales contenidas en esta composición y recupera la *n*-ésima pista virtual de esa ordenación.<br/> |
| [**GetRecursiveLayerOfTypeI**](iamtimelinecomp-getrecursivelayeroftypei.md) | No se admite.<br/>                                                                                                                                 |
| [**GetVTrack**](iamtimelinecomp-getvtrack.md)                               | Recupera la pista virtual con la prioridad especificada.<br/>                                                                                         |
| [**VTrackGetCount**](iamtimelinecomp-vtrackgetcount.md)                     | Recupera el número de pistas virtuales contenidas en la composición.<br/>                                                                           |
| [**VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md)                   | Inserta una pista virtual en la composición con la prioridad especificada.<br/>                                                                        |
| [**VTrackSwapPriorities**](iamtimelinecomp-vtrackswappriorities.md)         | Cambia los niveles de prioridad de dos pistas.<br/>                                                                                                    |



 

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



 

 
