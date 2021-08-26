---
title: BCM_GETSPLITINFO mensaje (Commctrl.h)
description: Obtiene información para un control de botón de división. Envíe este mensaje explícitamente o mediante la \_ macro Button GetSplitInfo.
ms.assetid: d608440d-b8d8-4e32-9128-08b7566b185c
keywords:
- BCM_GETSPLITINFO controles de Windows mensaje
topic_type:
- apiref
api_name:
- BCM_GETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ee0771c8999c6a805931a93ed28c245082d18e538856fde42b69622ee73f9a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921645"
---
# <a name="bcm_getsplitinfo-message"></a>Mensaje \_ GETSPLITINFO de BCM

Obtiene información para un control de botón de división. Envíe este mensaje explícitamente o mediante la macro [**\_ Button GetSplitInfo.**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura \_ BUTTON SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) para recibir información sobre el botón. El autor de la llamada es responsable de asignar la memoria para la estructura . Establezca el **miembro mask** de esta estructura para determinar qué información se va a recibir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Comentarios

Use este mensaje solo con los estilos [**de botón \_ BS SPLITBUTTON**](button-styles.md) y [**BS \_ DEFSPLITBUTTON.**](button-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



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

 

 





