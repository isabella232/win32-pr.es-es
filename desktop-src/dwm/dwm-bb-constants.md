---
title: Desenfoque de DWM detrás de constantes (Dwmapi.h)
description: Marcas usadas por la estructura \_ DWM BLURBEHIND para indicar cuál de sus miembros contiene información válida.
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
ms.openlocfilehash: d714fadce30748d337f9b6ff7a0d0aee59dbcb61e12744141c25bb78f07fa69c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094615"
---
# <a name="dwm-blur-behind-constants"></a>Desenfoque de DWM detrás de constantes

Marcas usadas por la [**estructura \_ DWM BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) para indicar cuál de sus miembros contiene información válida.

<dl> <dt>

<span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**DWM \_ BB \_ ENABLE**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Se ha especificado un valor para el miembro **fEnable.**


</dt> </dl> </dd> <dt>

<span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**DWM \_ BB \_ BLURREGION**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Se ha especificado un valor para el **miembro hRgnBlur.**


</dt> </dl> </dd> <dt>

<span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**DWM \_ BB \_ TRANSITIONONMAXIMIZED**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Se ha especificado un valor para el miembro **fTransitionOnMaximized.**


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Dwmapi.h</dt> </dl> |



 

 





