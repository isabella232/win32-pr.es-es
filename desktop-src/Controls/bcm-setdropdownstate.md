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
ms.openlocfilehash: fc44ec58d40e047708591121f81c84f327ca47c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170118"
---
# <a name="bcm_setdropdownstate-message"></a>Mensaje \_ SETDROPDOWNSTATE de BCM

Establece el estado desplegable de un botón con el estilo [**TBSTYLE \_ DROPDOWN**](toolbar-control-and-button-styles.md). Envíe este mensaje explícitamente o mediante la macro [**\_ Button SetDropDownState.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Un **VALOR BOOL** que es **TRUE** para el estado de BST \_ DROPDOWNPUSHED o **FALSE en** caso contrario.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[Estilos de botón](button-styles.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Tipos de botón](button-types-and-styles.md)
</dt> </dl>

 

 





