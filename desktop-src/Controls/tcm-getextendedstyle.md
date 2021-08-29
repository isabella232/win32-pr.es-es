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
ms.openlocfilehash: be5c4618fe039fcd05a73e409f0e8ddd7042694d526f902d432d2513bbef96e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876575"
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
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TCM \_ SETEXTENDEDSTYLE**](tcm-setextendedstyle.md)
</dt> </dl>

 

 





