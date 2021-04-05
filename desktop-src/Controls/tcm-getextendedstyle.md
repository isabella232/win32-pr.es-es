---
title: Mensaje de TCM_GETEXTENDEDSTYLE (commctrl. h)
description: Recupera los estilos extendidos que están actualmente en uso para el control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetExtendedStyle.
ms.assetid: 983ffcbe-0d8d-4686-83de-fc564744390f
keywords:
- TCM_GETEXTENDEDSTYLE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996963"
---
# <a name="tcm_getextendedstyle-message"></a>\_Mensaje GETEXTENDEDSTYLE de TCM

Recupera los estilos extendidos que están actualmente en uso para el control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **DWORD** que representa los estilos extendidos actualmente en uso para el control de ficha. Este valor es una combinación de [estilos extendidos](tab-control-extended-styles.md)de control de pestaña.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETEXTENDEDSTYLE TCM**](tcm-setextendedstyle.md)
</dt> </dl>

 

 





