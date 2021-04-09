---
description: A continuación se muestran las constantes de gestos.
ms.assetid: 21aaf8f0-13b7-4f97-ad4a-3557a7020337
title: Constantes de gestos (Tabflicks. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9a83f9a35a2c1a9cbd7c4b048a8c985f5eea34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154455"
---
# <a name="flicks-constants"></a>Gestos constantes

A continuación se muestran las constantes de gestos.



| Constante o valor                                                                                                                                                                                                                                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLICK_WM_HANDLED_MASK"></span><span id="flick_wm_handled_mask"></span><dl> <dt>**Gesto \_ de \_ \_ Máscara administrada de WM**</dt> <dt>0x1</dt> </dl> | Valor que se va a devolver después de controlar el mensaje de [**\_ mensaje de \_ gesto de Tablet PC de WM**](wm-tablet-flick-message.md) . Si se devuelve la **\_ \_ \_ máscara** superpuesto de WM, no se realiza ninguna otra acción. De lo contrario, Windows envía notificaciones de seguimiento, como [**WM \_ APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand), [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll)o [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown), dependiendo de la acción que esté asociada con el gesto de lápiz. <br/> |
| <span id="NUM_FLICK_DIRECTIONS"></span><span id="num_flick_directions"></span><dl> <dt>**Número \_ de \_Direcciones de gesto**</dt> <dt>8</dt> </dl>       | El número de direcciones definidas en la enumeración [**FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) .<br/>                                                                                                                                                                                                                                                                                                                                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Tabflicks. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Enumeración FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)
</dt> <dt>

[**\_Mensaje de gesto de Tablet PC de WM \_**](wm-tablet-flick-message.md)
</dt> <dt>

[Gestos de gestos](flicks-gestures.md)
</dt> <dt>

[Responder a gestos de lápiz](/previous-versions//dd356077(v=vs.85))
</dt> </dl>

 

