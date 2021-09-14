---
title: TTM_UPDATETIPTEXT mensaje (Commctrl.h)
description: Establece el texto de información sobre herramientas de una herramienta.
ms.assetid: 2a7432dd-76f9-42b4-b639-178dce1d89ef
keywords:
- TTM_UPDATETIPTEXT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165825"
---
# <a name="ttm_updatetiptext-message"></a>Mensaje \_ UPDATETIPTEXT de TTM

Establece el texto de información sobre herramientas de una herramienta.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TOOLINFO.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) Los **miembros resst** **y lpszText** deben especificar el identificador de instancia y la dirección del texto. Los **miembros hwnd** **y uId** identifican la herramienta que se debe actualizar. El **miembro cbSize** de esta estructura debe rellenarse antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTM \_ UPDATETIPTEXTW** (Unicode) y **TTM \_ UPDATETIPTEXTA** (ANSI)<br/>       |



 

 





