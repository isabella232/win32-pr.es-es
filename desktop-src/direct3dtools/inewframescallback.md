---
description: Devolución de llamada del motor que indica que se ha realizado el análisis de los fotogramas nuevos agregados al registro.
MS-HAID: vspixengine.INewFramesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: INewFramesCallback (interfaz)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A73E1EA4-F9D5-43F1-B363-20B3F7B3D8B0
api_name:
- INewFramesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8f9d47e84cf4deeebafa6592853f73e86d8339f8
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/24/2021
ms.locfileid: "122787321"
---
# <a name="span-idvspixengineinewframescallbackspaninewframescallback-interface"></a><span id="vspixengine.inewframescallback"></span>INewFramesCallback (interfaz)

Devolución de llamada del motor que indica que se ha realizado el análisis de los fotogramas nuevos agregados al registro.

## <a name="members"></a>Members

La **interfaz INewFramesCallback** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INewFramesCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

La **interfaz INewFramesCallback** tiene estos métodos.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Método</th><th >Descripción</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>CancelAll</strong></a></td><td ><p>Devolución de llamada que notifica al host que se han cancelado todas las solicitudes.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>CancelUsingCallback</strong></a></td><td ><p>Devolución de llamada que notifica al host de una solicitud cancelada.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>CancelUsingCookie</strong></a></td><td ><p>Devolución de llamada que notifica al host de una solicitud cancelada mediante una cookie que identifica de forma única la solicitud.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>NewFramesAvailable</strong></a></td><td ><p>Devolución de llamada que notifica al host que hay nuevos fotogramas disponibles para procesarse.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
