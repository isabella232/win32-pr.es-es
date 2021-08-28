---
description: La devolución de llamada a devuelve datos de análisis sin conexión.
MS-HAID: vspixengine.IOfflineAnalysisCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IOfflineAnalysisCallback (interfaz)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 39E6B9CA-C17A-42C8-AC6D-118DC8DE3AD9
api_name:
- IOfflineAnalysisCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e7d21b134230c86a91a49d1d323c96da74cfb150
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786581"
---
# <a name="span-idvspixengineiofflineanalysiscallbackspaniofflineanalysiscallback-interface"></a><span id="vspixengine.iofflineanalysiscallback"></span>IOfflineAnalysisCallback (interfaz)

La devolución de llamada a devuelve datos de análisis sin conexión.

## <a name="members"></a>Members

La **interfaz IOfflineAnalysisCallback** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IOfflineAnalysisCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

La **interfaz IOfflineAnalysisCallback** tiene estos métodos.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Método</th><th >Descripción</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysiscomplete-dword-hresult-bstr"><strong>OfflineAnalysisComplete</strong></a></td><td ><p>Función de devolución de llamada que se usa para notificar al host que se ha completado el análisis sin conexión.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysisprogress-dword-double"><strong>OfflineAnalysisProgress</strong></a></td><td ><p>Función de devolución de llamada que se usa para notificar al host el progreso del análisis sin conexión.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
