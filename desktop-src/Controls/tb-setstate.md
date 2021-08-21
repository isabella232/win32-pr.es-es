---
title: TB_SETSTATE mensaje (Commctrl.h)
description: Establece el estado del botón especificado en una barra de herramientas.
ms.assetid: 68633b58-8d21-4931-b01f-32a66bda37b1
keywords:
- TB_SETSTATE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa9ee112e4bbbe9c64ceab6205d67ecd6ae9653df97be55991be38eb5d181d3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167475"
---
# <a name="tb_setstate-message"></a>Mensaje \_ SETSTATE de TB

Establece el estado del botón especificado en una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón.

</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD [**es una combinación**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de valores enumerados en Estados del botón de la barra de [herramientas](toolbar-button-states.md). HIWORD [**debe**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

