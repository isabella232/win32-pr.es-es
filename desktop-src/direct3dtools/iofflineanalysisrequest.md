---
description: Solicitar datos de análisis sin conexión.
MS-HAID: vspixengine.IOfflineAnalysisRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IOfflineAnalysisRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1E438545-D4C4-45A7-918E-D3D9DC06BA08
api_name:
- IOfflineAnalysisRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 980c4d9f3b745d197789e5e450e0bf782127ca0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906751"
---
# <a name="span-idvspixengineiofflineanalysisrequestspaniofflineanalysisrequest-interface"></a><span id="vspixengine.iofflineanalysisrequest"></span>Interfaz IOfflineAnalysisRequest

Solicitar datos de análisis sin conexión.

## <a name="members"></a>Miembros

La interfaz **IOfflineAnalysisRequest** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IOfflineAnalysisRequest** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

La interfaz **IOfflineAnalysisRequest** tiene estos métodos.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Método</th><th style="text-align: left;">Descripción</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-cancelofflineanalysisasync-dword"><strong>CancelOfflineAnalysisAsync</strong></a></td><td style="text-align: left;"><p>Solicitudes para cancelar el análisis sin conexión en una solicitud de análisis sin conexión.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-requestofflineanalysisasync-enumofflineanalysissource-bstr-bstr-dword-bstr-dword-bstr-iofflineanalysiscallback-ptr"><strong>RequestOfflineAnalysisAsync</strong></a></td><td style="text-align: left;"><p>Solicita que se ejecute el análisis sin conexión con el origen especificado, el manifiesto, los parámetros y el marco especificado.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
