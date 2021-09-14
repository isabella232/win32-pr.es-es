---
title: TTM_NEWTOOLRECT mensaje (Commctrl.h)
description: Establece un nuevo rectángulo delimitador para una herramienta.
ms.assetid: 81d1b745-310e-482e-8c6e-6e98e1e67b66
keywords:
- TTM_NEWTOOLRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TTM_NEWTOOLRECT
- TTM_NEWTOOLRECTA
- TTM_NEWTOOLRECTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75417059b0108877d04c79af25ac98245461ad5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165885"
---
# <a name="ttm_newtoolrect-message"></a>MENSAJE \_ DE NEWTOOLRECT de TTM

Establece un nuevo rectángulo delimitador para una herramienta.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TOOLINFO.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) Los **miembros hwnd** **y uId** identifican una herramienta y el **miembro rect** especifica el nuevo rectángulo delimitador. El **miembro cbSize** de esta estructura debe rellenarse antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTM \_ NEWTOOLRECTW** (Unicode) y **TTM \_ NEWTOOLRECTA** (ANSI)<br/>           |



 

 





