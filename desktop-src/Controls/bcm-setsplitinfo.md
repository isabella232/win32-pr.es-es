---
title: Mensaje de BCM_SETSPLITINFO (commctrl. h)
description: Establece la información de un control de botón de expansión. Envíe este mensaje explícitamente o mediante la \_ macro Button SetSplitInfo.
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- BCM_SETSPLITINFO controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658213"
---
# <a name="bcm_setsplitinfo-message"></a>\_Mensaje SETSPLITINFO de BCM

Establece la información de un control de botón de expansión. Envíe este mensaje explícitamente o mediante la macro [**Button \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Puntero a una estructura [**\_ SPLITINFO de botón**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) que contiene información sobre el botón de expansión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Use este mensaje solo con los estilos de botón [**BS \_ SPLITBUTTON**](button-styles.md) y [**BS \_ DEFSPLITBUTTON**](button-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[Estilos de botón](button-styles.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Tipos de botón](button-types-and-styles.md)
</dt> </dl>

 

 





