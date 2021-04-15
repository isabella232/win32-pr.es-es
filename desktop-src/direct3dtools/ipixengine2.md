---
description: Extensiones de la interfaz IPixEngine original.
MS-HAID: vspixengine.IPixEngine2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IPixEngine2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D650FB4C-C332-4E2E-85EB-DDCE3DA87B0C
api_name:
- IPixEngine2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bf8fe4537a6f4c8703482289302ffa8f3a645903
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494693"
---
# <a name="span-idvspixengineipixengine2spanipixengine2-interface"></a><span id="vspixengine.ipixengine2"></span>Interfaz IPixEngine2

Extensiones de la interfaz IPixEngine original.

## <a name="members"></a>Miembros

La interfaz **IPixEngine2** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPixEngine2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

La interfaz **IPixEngine2** tiene estos métodos.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Método</th><th style="text-align: left;">Descripción</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine2-endexperiment-bstr-ifileiocallback-ptr"><strong>EndExperiment</strong></a></td><td style="text-align: left;"><p>Finaliza el experiement y completa el registro de gráficos.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine2-getplaybackmachine-bstr-bool-ptr-bstr-ptr"><strong>GetPlaybackMachine</strong></a></td><td style="text-align: left;"><p>Obtiene información sobre el equipo de reproducción actual.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine2-onnewdataavailable-bool-bool-int64-int64-int32-byte-arr"><strong>OnNewDataAvailable</strong></a></td><td style="text-align: left;"><p>Solicitudes para indicar que el registro de gráficos tiene nuevos datos dentro de él.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine2-setplaybackmachine-bstr-bool-bstr"><strong>SetPlaybackMachine</strong></a></td><td style="text-align: left;"><p>Establece el equipo de reproducción actual para el registro de gráficos especificado.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
