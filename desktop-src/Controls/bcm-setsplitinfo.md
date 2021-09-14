---
title: BCM_SETSPLITINFO mensaje (Commctrl.h)
description: Establece la información de un control de botón de división. Envíe este mensaje explícitamente o mediante la macro \_ Button SetSplitInfo.
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- BCM_SETSPLITINFO controles de Windows mensaje
topic_type:
- apiref
api_name:
- BCM_SETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac40f2d1ef016ee76ab21ccf2dc4733d0ff427f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968735"
---
# <a name="bcm_setsplitinfo-message"></a>Mensaje \_ SETSPLITINFO de BCM

Establece la información de un control de botón de división. Envíe este mensaje explícitamente o mediante la macro [**\_ Button SetSplitInfo.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Puntero a una [**estructura BUTTON \_ SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) que contiene información sobre el botón de división.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Observaciones

Use este mensaje solo con los estilos [**de botón \_ BS SPLITBUTTON**](button-styles.md) y [**BS \_ DEFSPLITBUTTON.**](button-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[Estilos de botón](button-styles.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Tipos de botón](button-types-and-styles.md)
</dt> </dl>

 

 





