---
title: TB_INDETERMINATE mensaje (Commctrl.h)
description: Establece o borra el estado indeterminado del botón especificado en una barra de herramientas.
ms.assetid: 6a0f2b82-8241-4c2e-b349-606975ba1a24
keywords:
- TB_INDETERMINATE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166729"
---
# <a name="tb_indeterminate-message"></a>Mensaje \_ INDETERMINADO de TB

Establece o borra el estado indeterminado del botón especificado en una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón cuyo estado indeterminado se va a establecer o borrar.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD es**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un **BOOL** que indica si se debe establecer o borrar el estado indeterminado. Si **es TRUE,** se establece el estado indeterminado. Si **es FALSE,** el estado se borra.

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



 

