---
title: TB_SETPADDING mensaje (Commctrl.h)
description: Establece el relleno de un control de barra de herramientas.
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- TB_SETPADDING controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166578"
---
# <a name="tb_setpadding-message"></a>Mensaje \_ SETPADDING de TB

Establece el relleno de un control de barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el relleno horizontal, en píxeles. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el relleno vertical, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor DWORD** que contiene el relleno horizontal anterior en [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y el relleno vertical anterior en [**HIWORD,**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))en píxeles.

## <a name="remarks"></a>Observaciones

Los valores de relleno se usan para crear un área en blanco entre el borde del botón y la imagen o el texto del botón. El lugar y la cantidad de relleno que se aplica realmente depende del tipo del botón y de si tiene una imagen. El relleno horizontal se aplica tanto a la derecha como a la izquierda del botón, y el relleno vertical se aplica tanto a la parte superior como a la parte inferior del botón. El relleno solo se aplica a los botones que tienen el [**estilo TBSTYLE \_ AUTOSIZE.**](toolbar-control-and-button-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TB \_ GETPADDING**](tb-getpadding.md)
</dt> </dl>

 

