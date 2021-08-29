---
description: Devolución de llamada para devolver intersecciones del historial de píxeles (nivel de llamada de dibujo) y primitivas (nivel de triángulo) en dos resultados diferentes.
MS-HAID: vspixengine.IPixelHistoryCallback2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IPixelHistoryCallback2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0111482E-B66A-4763-8890-85B1711F38B2
api_name:
- IPixelHistoryCallback2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dab9359d117043ee0902df8869a3cf9bb8f30b27
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/24/2021
ms.locfileid: "122787181"
---
# <a name="span-idvspixengineipixelhistorycallback2spanipixelhistorycallback2-interface"></a><span id="vspixengine.ipixelhistorycallback2"></span>Interfaz IPixelHistoryCallback2

Devolución de llamada para devolver intersecciones del historial de píxeles (nivel de llamada de dibujo) y primitivas (nivel de triángulo) en dos resultados diferentes.

## <a name="members"></a>Members

La **interfaz IPixelHistoryCallback2** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPixelHistoryCallback2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

La **interfaz IPixelHistoryCallback2** tiene estos métodos.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Método</th><th >Descripción</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-intersectionscallback-dword-pixelhistoryintersection-arr"><strong>IntersectionsCallback</strong></a></td><td ><p>Devolución de llamada que notifica al host la información de intersección del historial de píxeles devuelta por la solicitud asocaited.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-primitivescallback-dword-pixelhistoryoperation-arr"><strong>PrimitivesCallback</strong></a></td><td ><p>Devolución de llamada que notifica al host la información de operación primitiva del historial de píxeles devuelta por la solicitud asociada.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
