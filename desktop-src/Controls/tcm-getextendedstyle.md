---
title: TCM_GETEXTENDEDSTYLE mensaje (Commctrl.h)
description: Recupera los estilos extendidos que están actualmente en uso para el control de ficha. Puede enviar este mensaje explícitamente o mediante la macro \_ TabCtrl GetExtendedStyle.
ms.assetid: 983ffcbe-0d8d-4686-83de-fc564744390f
keywords:
- TCM_GETEXTENDEDSTYLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8280b7043591dd4fdd0b453c5baea5fe014bd3d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166269"
---
# <a name="tcm_getextendedstyle-message"></a>Mensaje \_ GETEXTENDEDSTYLE de TCM

Recupera los estilos extendidos que están actualmente en uso para el control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**\_ TabCtrl GetExtendedStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor DWORD** que representa los estilos extendidos actualmente en uso para el control de ficha. Este valor es una combinación de estilos extendidos de control [de tabulación.](tab-control-extended-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TCM \_ SETEXTENDEDSTYLE**](tcm-setextendedstyle.md)
</dt> </dl>

 

 





