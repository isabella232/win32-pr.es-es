---
description: Devolución de llamada para devolver un destino de representación. El formato del destino de representación devuelto es R8G8B8A8 UNORM independientemente del formato del destino de \_ representación en el motor.
MS-HAID: vspixengine.IFrameBufferCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameBufferCallback (interfaz)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 613AD7AC-0732-49E2-8155-AE0A76597BE9
api_name:
- IFrameBufferCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 479796ebf225ceac4e93f429aa6b8412e3f86398
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628843"
---
# <a name="span-idvspixengineiframebuffercallbackspaniframebuffercallback-interface"></a><span id="vspixengine.iframebuffercallback"></span>IFrameBufferCallback (interfaz)

Devolución de llamada para devolver un destino de representación. El formato del destino de representación devuelto es R8G8B8A8 UNORM independientemente del formato del destino de \_ representación en el motor.

## <a name="members"></a>Miembros

La **interfaz IFrameBufferCallback** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IFrameBufferCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

La **interfaz IFrameBufferCallback** tiene estos métodos.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">Método</th><th style="text-align: left;">Descripción</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ResultCallback</strong></a></td><td style="text-align: left;"><p>Devolución de llamada que notifica al host la información de framebuffer devuelta por la solicitud asociada.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
