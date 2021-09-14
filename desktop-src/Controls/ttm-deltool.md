---
title: TTM_DELTOOL mensaje (Commctrl.h)
description: Quita una herramienta de un control de información sobre herramientas.
ms.assetid: 433b6f1c-3e9f-4e3a-9834-d447a3f9e6a5
keywords:
- TTM_DELTOOL controles de Windows mensaje
topic_type:
- apiref
api_name:
- TTM_DELTOOL
- TTM_DELTOOLA
- TTM_DELTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943259c5496757c0f15ca4127d0a5e6a4237fbe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165937"
---
# <a name="ttm_deltool-message"></a>Mensaje \_ DELTOOL de TTM

Quita una herramienta de un control de información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TOOLINFO.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) Los **miembros hwnd** **y uId** identifican la herramienta que se quitará y el **miembro cbSize** debe especificar el tamaño de la estructura. Se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTM \_ DELTOOLW** (Unicode) y **TTM \_ DELTOOLA** (ANSI)<br/>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TTM \_ ADDTOOL**](ttm-addtool.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Acerca de los controles de información sobre herramientas](tooltip-controls.md)
</dt> </dl>

 

 





