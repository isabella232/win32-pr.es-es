---
description: Representa información sobre una solicitud del depurador de sombreador.
MS-HAID: vspixengine.DebugShaderRequestInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: DebugShaderRequestInfo (estructura)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DEFFAEE4-6C53-4C89-A533-A5BE73B80DEA
api_name:
- DebugShaderRequestInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f0698782b9829f752ecb1fd45c4baf7794a206c8a7162e1f960cc550012b8532
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283952"
---
# <a name="span-idvspixenginedebugshaderrequestinfospandebugshaderrequestinfo-structure"></a><span id="vspixengine.debugshaderrequestinfo"></span>DebugShaderRequestInfo (estructura)

Representa información sobre una solicitud del depurador de sombreador.

## <a name="syntax"></a>Sintaxis


```C++
} DebugShaderRequestInfo;
```

## <a name="members"></a>Miembros

**Etapa**  
Fase de canalización que se depura.

**Eventid**  
Identificador del evento de gráficos que se depura.

**frameNumber**  
Marco que se depura.

**Vértice**  
Vértice que se depura.

**Pixel**  
Píxel que se depura.

**groupCoordinates**  
Coordenadas del grupo que se depura.

**threadCoordinates**  
Coordenadas del subproceso que se depura

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



