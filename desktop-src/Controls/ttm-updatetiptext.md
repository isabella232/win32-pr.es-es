---
title: Mensaje de TTM_UPDATETIPTEXT (commctrl. h)
description: Establece el texto de la información sobre herramientas de una herramienta.
ms.assetid: 2a7432dd-76f9-42b4-b639-178dce1d89ef
keywords:
- TTM_UPDATETIPTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_UPDATETIPTEXT
- TTM_UPDATETIPTEXTA
- TTM_UPDATETIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c94b14ec83c190ce019ecba1413d2fa05f0103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150537"
---
# <a name="ttm_updatetiptext-message"></a>TTM \_ UPDATETIPTEXT

Establece el texto de la información sobre herramientas de una herramienta.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . Los miembros **HINST** y **lpszText** deben especificar el identificador de instancia y la dirección del texto. Los miembros **hWnd** y **uId** identifican la herramienta que se va a actualizar. El miembro **cbSize** de esta estructura se debe rellenar antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTM \_ UPDATETIPTEXTW** (Unicode) y **TTM \_ UPDATETIPTEXTA** (ANSI)<br/>       |



 

 





