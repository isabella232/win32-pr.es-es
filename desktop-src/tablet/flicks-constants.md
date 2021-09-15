---
description: Las siguientes son las constantes Flicks.
ms.assetid: 21aaf8f0-13b7-4f97-ad4a-3557a7020337
title: Constantes flicks (Tabflicks.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9a83f9a35a2c1a9cbd7c4b048a8c985f5eea34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360318"
---
# <a name="flicks-constants"></a>Constantes de gestos

Las siguientes son las constantes Flicks.



| Constante o valor                                                                                                                                                                                                                                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLICK_WM_HANDLED_MASK"></span><span id="flick_wm_handled_mask"></span><dl> <dt>**FLICK \_ Máscara de wm \_ \_ handled mask**</dt> <dt>0x1</dt> </dl> | Valor que se devuelve después de controlar el [**mensaje WM \_ TABLET \_ FLICK.**](wm-tablet-flick-message.md) Si **se devuelve FLICK WM \_ \_ HANDLED \_ MASK,** no se produce ninguna otra acción. De lo contrario, Windows notificaciones de seguimiento, como [**WM \_ APPCOMMAND,**](/windows/desktop/inputdev/wm-appcommand) [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll)o [**WM \_ KEYDOWN,**](/windows/desktop/inputdev/wm-keydown)en función de la acción asociada al gesto de lápiz. <br/> |
| <span id="NUM_FLICK_DIRECTIONS"></span><span id="num_flick_directions"></span><dl> <dt>**NUM \_ FLICK \_ DIRECTIONS**</dt> <dt>8</dt> </dl>       | Número de direcciones definidas en la [**enumeración FLICKDIRECTION.**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)<br/>                                                                                                                                                                                                                                                                                                                                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Tabflicks.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ENUMERACIÓN FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)
</dt> <dt>

[**Mensaje \_ WM TABLET \_ FLICK**](wm-tablet-flick-message.md)
</dt> <dt>

[Gestos de gestos de gestos](flicks-gestures.md)
</dt> <dt>

[Respuesta a pen flicks](/previous-versions//dd356077(v=vs.85))
</dt> </dl>

 

