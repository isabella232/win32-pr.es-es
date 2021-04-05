---
title: Mensaje de TB_INDETERMINATE (commctrl. h)
description: Establece o borra el estado indeterminado del botón especificado en una barra de herramientas.
ms.assetid: 6a0f2b82-8241-4c2e-b349-606975ba1a24
keywords:
- TB_INDETERMINATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_INDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f1de35f9621de4f51d371bb50dbda637d720cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079197"
---
# <a name="tb_indeterminate-message"></a>TB de \_ mensaje indeterminado

Establece o borra el estado indeterminado del botón especificado en una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón cuyo estado indeterminado se va a establecer o borrar.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un valor **booleano** que indica si se debe establecer o borrar el estado indeterminado. Si es **true**, se establece el estado indeterminado. Si es **false**, el estado es desactivado.

El valor de [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

