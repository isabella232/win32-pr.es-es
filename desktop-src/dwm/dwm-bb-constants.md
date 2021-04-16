---
title: Desenfoque de DWM en las constantes (dwmapi. h)
description: Marcas usadas por la \_ estructura BLURBEHIND de DWM para indicar cuál de sus miembros contiene información válida.
ms.assetid: d6dd552c-1f3b-4f16-8705-f5016ed55d9e
topic_type:
- apiref
api_name:
- DWM_BB_ENABLE
- DWM_BB_BLURREGION
- DWM_BB_TRANSITIONONMAXIMIZED
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe08e0315d4c4b906cdb897ac7ad5dd34d50fbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534516"
---
# <a name="dwm-blur-behind-constants"></a>Desenfoque de DWM detrás de constantes

Marcas usadas por la [**estructura \_ BLURBEHIND de DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) para indicar cuál de sus miembros contiene información válida.

<dl> <dt>

<span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**DWM \_ BB \_ habilitado**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Se ha especificado un valor para el miembro **fEnable** .


</dt> </dl> </dd> <dt>

<span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**DWM \_ BB \_ BLURREGION**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Se ha especificado un valor para el miembro **hRgnBlur** .


</dt> </dl> </dd> <dt>

<span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**DWM \_ BB \_ TRANSITIONONMAXIMIZED**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Se ha especificado un valor para el miembro **fTransitionOnMaximized** .


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Dwmapi. h</dt> </dl> |



 

 





