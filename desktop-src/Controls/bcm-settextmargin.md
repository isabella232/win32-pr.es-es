---
title: Mensaje de BCM_SETTEXTMARGIN (commctrl. h)
description: El \_ mensaje SETTEXTMARGIN de BCM establece los márgenes para dibujar texto en un control de botón.
ms.assetid: 0798b1c5-7db4-46c6-8881-4c847abc7460
keywords:
- BCM_SETTEXTMARGIN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BCM_SETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb6653007c155a508ce4da899a7be0d8ff2ab2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490552"
---
# <a name="bcm_settextmargin-message"></a>\_Mensaje SETTEXTMARGIN de BCM

El **mensaje \_ SETTEXTMARGIN de BCM** establece los márgenes para dibujar texto en un control de botón.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica los márgenes que se van a usar para dibujar el texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, devuelve **true**. En caso contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**Botón \_ SetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_settextmargin)
</dt> <dt>

**Vista**
</dt> <dt>

[Botones](buttons.md)
</dt> </dl>

 

