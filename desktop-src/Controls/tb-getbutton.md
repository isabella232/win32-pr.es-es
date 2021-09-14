---
title: TB_GETBUTTON mensaje (Commctrl.h)
description: Recupera información sobre el botón especificado en una barra de herramientas.
ms.assetid: d90d053c-0daf-4a5a-b7ca-b9b4472c65a3
keywords:
- TB_GETBUTTON controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_GETBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2080a6c984bb2384f68a1388bd46fe598f5087
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166857"
---
# <a name="tb_getbutton-message"></a>Mensaje \_ GETBUTTON de TB

Recupera información sobre el botón especificado en una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del botón para el que se va a recuperar información.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la [**estructura TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que recibe la información del botón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





