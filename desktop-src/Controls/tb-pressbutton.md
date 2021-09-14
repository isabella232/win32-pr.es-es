---
title: TB_PRESSBUTTON mensaje (Commctrl.h)
description: Presiona o suelta el botón especificado en una barra de herramientas.
ms.assetid: 03f6c3c2-d679-4e3a-a07b-c7e46c97972a
keywords:
- TB_PRESSBUTTON controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_PRESSBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0e86092951b242cee7388fc0d5d1bbdbca835e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166678"
---
# <a name="tb_pressbutton-message"></a>Mensaje \_ PRESSBUTTON de TB

Presiona o suelta el botón especificado en una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón que se debe presionar o liberar.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD es**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un **BOOL** que indica si se debe presionar o liberar el botón especificado. Si **es TRUE,** se presiona el botón. Si **es FALSE,** se libera el botón.

HIWORD [**debe**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

