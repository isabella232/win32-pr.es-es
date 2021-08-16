---
title: BCM_SETDROPDOWNSTATE mensaje (Commctrl.h)
description: Establece el estado desplegable de un botón con el estilo TBSTYLE \_ DROPDOWN. Envíe este mensaje explícitamente o mediante la macro \_ Button SetDropDownState.
ms.assetid: 725deff4-0bcb-497d-a6cf-e9c98b05f16e
keywords:
- BCM_SETDROPDOWNSTATE controles de Windows mensaje
topic_type:
- apiref
api_name:
- BCM_SETDROPDOWNSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 989b4a04502a730c06a906be28a6915a4e604ff22c4b4e5ae9a4b85c8b464f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117833636"
---
# <a name="bcm_setdropdownstate-message"></a>Mensaje \_ SETDROPDOWNSTATE de BCM

Establece el estado desplegable de un botón con el estilo [**TBSTYLE \_ DROPDOWN**](toolbar-control-and-button-styles.md). Envíe este mensaje explícitamente o mediante la macro [**\_ Button SetDropDownState.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Un **VALOR BOOL** que es **TRUE para** el estado de BST \_ DROPDOWNPUSHED o **FALSE** en caso contrario.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



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

 

 





