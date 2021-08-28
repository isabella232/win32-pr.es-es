---
description: Devolución de llamada para devolver las versiones de todas las interfaces admitidas. Esto permite que el consumidor no esté sincronizado con el motor de captura.
MS-HAID: vspixengine.IVersionCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IVersionCallback (interfaz)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7135E175-C537-4B0C-8F0A-CB77E3F2D945
api_name:
- IVersionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 905c6f085695ba20b7cdd3a363c3af5a833d598a
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/24/2021
ms.locfileid: "122787496"
---
# <a name="span-idvspixengineiversioncallbackspaniversioncallback-interface"></a><span id="vspixengine.iversioncallback"></span>IVersionCallback (interfaz)

Devolución de llamada para devolver las versiones de todas las interfaces admitidas. Esto permite que el consumidor no esté sincronizado con el motor de captura.

## <a name="members"></a>Members

La **interfaz IVersionCallback** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IVersionCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

La **interfaz IVersionCallback** tiene estos métodos.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Método</th><th >Descripción</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/iversioncallback-versiontableready-guid-arr-uint"><strong>VersionTableReady</strong></a></td><td ><p>Función de devolución de llamada que se usa para notificar al host de qué interfaces se admiten.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
