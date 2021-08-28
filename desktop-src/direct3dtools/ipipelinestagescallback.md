---
description: '<span id="vspixengine.ipipelinestagescallback"></span>Interfaz IPipeLineStagesCallback: no se usa. Anteriormente, una devolución de llamada para los datos de fases de canalización.'
MS-HAID: vspixengine.IPipeLineStagesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback (interfaz)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2F5B84DB-3D06-4D82-BF1D-E5853CC4B835
api_name:
- IPipeLineStagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2fc828d902f1daa3b2c0c75d2f22671d9bdec942
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/24/2021
ms.locfileid: "122787510"
---
# <a name="span-idvspixengineipipelinestagescallbackspanipipelinestagescallback-interface"></a><span id="vspixengine.ipipelinestagescallback"></span>IPipeLineStagesCallback (interfaz)

No se utiliza. Anteriormente, una devolución de llamada para los datos de fases de canalización.

## <a name="members"></a>Members

La **interfaz IPipeLineStagesCallback** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPipeLineStagesCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

La **interfaz IPipeLineStagesCallback** tiene estos métodos.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Método</th><th >Descripción</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></td><td ><p>Devolución de llamada que notifica al host qué fases de canalización se usan mediante la llamada draw de la solicitud asocaited.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></td><td ><p>Devolución de llamada que notifica al host de qué fases de canalización no pueden devolver datos de malla para el evento especificado en la solicitud asociada.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></td><td ><p>Devolución de llamada que notifica al host de las fases de canalización información de malla devuelta por la solicitud a la que se ha avisado.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></td><td ><p>Devolución de llamada que notifica al host de las fases de canalización información de imagen devuelta por la solicitud asocaited.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
