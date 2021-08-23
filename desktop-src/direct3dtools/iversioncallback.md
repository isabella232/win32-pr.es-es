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
ms.openlocfilehash: c3ff23d325ff7b9d2783c9e35ca523253cea2880453c46f94a7d915cb47e8f8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119419"
---
# <a name="span-idvspixengineiversioncallbackspaniversioncallback-interface"></a><span id="vspixengine.iversioncallback"></span>IVersionCallback (interfaz)

Devolución de llamada para devolver las versiones de todas las interfaces admitidas. Esto permite que el consumidor no esté sincronizado con el motor de captura.

## <a name="members"></a>Miembros

La **interfaz IVersionCallback** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IVersionCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

La **interfaz IVersionCallback** tiene estos métodos.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Método</th><th style="text-align: left;">Descripción</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iversioncallback-versiontableready-guid-arr-uint"><strong>VersionTableReady</strong></a></td><td style="text-align: left;"><p>Función de devolución de llamada que se usa para notificar al host de qué interfaces se admiten.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
