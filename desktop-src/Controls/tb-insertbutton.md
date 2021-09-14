---
title: TB_INSERTBUTTON mensaje (Commctrl.h)
description: Inserta un botón en una barra de herramientas.
ms.assetid: 6be27817-5d86-4649-bd63-173845197763
keywords:
- TB_INSERTBUTTON controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_INSERTBUTTON
- TB_INSERTBUTTONA
- TB_INSERTBUTTONW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e08eed328a99d4a8927a7e09084bf122f2e4e84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166726"
---
# <a name="tb_insertbutton-message"></a>Mensaje \_ INSERTBUTTON de TB

Inserta un botón en una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de un botón. El mensaje inserta el nuevo botón a la izquierda de este botón.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que contiene información sobre el botón que se insertará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TB \_ INSERTBUTTONW** (Unicode) y **TB \_ INSERTBUTTONA** (ANSI)<br/>           |



 

 





