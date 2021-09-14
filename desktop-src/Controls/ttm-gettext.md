---
title: TTM_GETTEXT mensaje (Commctrl.h)
description: Recupera la información que un control de información sobre herramientas mantiene sobre una herramienta.
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- TTM_GETTEXT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TTM_GETTEXT
- TTM_GETTEXTA
- TTM_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f774671d34f89306593d23481fa917190ae69aaa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165913"
---
# <a name="ttm_gettext-message"></a>Mensaje \_ GETTEXT de TTM

Recupera la información que un control de información sobre herramientas mantiene sobre una herramienta.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Número de **TCHAR**, incluido el valor **NULL** final, que se copiará en el búfer al que **apunta lpszText.** </dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TOOLINFO.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) Establezca el **miembro cbSize** de esta estructura en `sizeof(TOOLINFO)` antes de enviar este mensaje. Establezca los **miembros hwnd** **y uId** para identificar la herramienta para la que se va a recuperar información. Asigne un búfer de tamaño especificado por *wParam*. Establezca el **miembro lpszText** para que apunte al búfer para recibir el texto de la herramienta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTM \_ GETTEXTW** (Unicode) y **TTM \_ GETTEXTA** (ANSI)<br/>                   |



 

 





