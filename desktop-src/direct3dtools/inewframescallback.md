---
description: Devolución de llamada desde el motor que indica que se ha terminado de analizar los nuevos marcos agregados al registro.
MS-HAID: vspixengine.INewFramesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz INewFramesCallback
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
ms.openlocfilehash: 134de14d95ceb625f1c5d4461c0b379b7f9e8a0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423135"
---
# <a name="span-idvspixengineinewframescallbackspaninewframescallback-interface"></a><span id="vspixengine.inewframescallback"></span>Interfaz INewFramesCallback

Devolución de llamada desde el motor que indica que se ha terminado de analizar los nuevos marcos agregados al registro.

## <a name="members"></a>Miembros

La interfaz **INewFramesCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INewFramesCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

La interfaz **INewFramesCallback** tiene estos métodos.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Método</th><th style="text-align: left;">Descripción</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>CancelAll</strong></a></td><td style="text-align: left;"><p>Devolución de llamada que notifica al host que se han cancelado todas las solicitudes.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>CancelUsingCallback</strong></a></td><td style="text-align: left;"><p>Devolución de llamada que notifica al host de una solicitud cancelada.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>CancelUsingCookie</strong></a></td><td style="text-align: left;"><p>Devolución de llamada que notifica al host de una solicitud cancelada mediante una cookie que identifica de forma única la solicitud.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>NewFramesAvailable</strong></a></td><td style="text-align: left;"><p>Devolución de llamada que notifica al host que hay nuevos marcos disponibles para su procesamiento.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
