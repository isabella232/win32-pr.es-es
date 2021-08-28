---
description: Devoluciones de llamada usadas para ver texturas.
MS-HAID: vspixengine.IPixEngine5Callbacks
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IPixEngine5Callbacks
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F87F00ED-C816-49A3-926B-28E3C8330EA2
api_name:
- IPixEngine5Callbacks
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 75124025c2857f98f71934b1e3848b3b7ac186ac
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786311"
---
# <a name="span-idvspixengineipixengine5callbacksspanipixengine5callbacks-interface"></a><span id="vspixengine.ipixengine5callbacks"></span>Interfaz IPixEngine5Callbacks

Devoluciones de llamada usadas para ver texturas.

## <a name="members"></a>Members

La **interfaz IPixEngine5Callbacks** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPixEngine5Callbacks** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

La **interfaz IPixEngine5Callbacks** tiene estos métodos.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Método</th><th >Descripción</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>FreeTextureComplete</strong></a></td><td ><p>Función de devolución de llamada que se usa para notificar al host cuando se ha liberando una textura.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>LoadHistogramComplete</strong></a></td><td ><p>Función de devolución de llamada que se usa para notificar al host cuando se ha completado una carga de histograma.</p></td></tr><tr class="odd"><td ><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>LoadTextureFromFileComplete</strong></a></td><td ><p>Función de devolución de llamada que se usa para notificar al host cuando se ha completado una carga de textura.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>LoadTextureSliceComplete</strong></a></td><td ><p>Función de devolución de llamada que se usa para notificar al host cuando se ha completado una carga de segmento de textura.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>ReadTexelValueComplete</strong></a></td><td ><p>Función de devolución de llamada que se usa para notificar al host cuando se ha completado una lectura de valores de textura.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>RenderTextureComplete</strong></a></td><td ><p>Función de devolución de llamada que se usa para notificar al host cuando se ha completado una representación de textura.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>SaveTextureComplete</strong></a></td><td ><p>Función de devolución de llamada que se usa para notificar al host cuando se ha completado el guardado de una textura.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
