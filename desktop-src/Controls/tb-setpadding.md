---
title: Mensaje de TB_SETPADDING (commctrl. h)
description: Establece el relleno de un control de barra de herramientas.
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- TB_SETPADDING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65fae53f7e7702528915af7631bd675f11188b71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150976"
---
# <a name="tb_setpadding-message"></a>\_Mensaje SETPADDING TB

Establece el relleno de un control de barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el relleno horizontal, en píxeles. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el relleno vertical, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **DWORD** que contiene el relleno horizontal anterior en el [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y el relleno vertical anterior en el [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), en píxeles.

## <a name="remarks"></a>Observaciones

Los valores de relleno se usan para crear un área en blanco entre el borde del botón y la imagen o el texto del botón. Dónde y cuánto relleno se aplica realmente depende del tipo del botón y de si tiene una imagen. El relleno horizontal se aplica a la derecha y a la izquierda del botón, y el relleno vertical se aplica a la parte superior e inferior del botón. El relleno solo se aplica a los botones que tienen el estilo de [**\_ ajuste automático de TBSTYLE**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TB \_ GETPADDING**](tb-getpadding.md)
</dt> </dl>

 

