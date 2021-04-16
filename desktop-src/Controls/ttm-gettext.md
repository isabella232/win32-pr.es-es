---
title: Mensaje de TTM_GETTEXT (commctrl. h)
description: Recupera la información que un control ToolTip mantiene sobre una herramienta.
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- TTM_GETTEXT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658188"
---
# <a name="ttm_gettext-message"></a>Mensaje de TTM \_ GETTEXT

Recupera la información que un control ToolTip mantiene sobre una herramienta.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Número de **TCHARs**, incluido el **valor null** final, que se va a copiar en el búfer al que apunta **lpszText**. </dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . Establezca el miembro **cbSize** de esta estructura en `sizeof(TOOLINFO)` antes de enviar este mensaje. Establezca los miembros **hWnd** y **uId** para identificar la herramienta para la que se va a recuperar información. Asigna un búfer de tamaño especificado por *wParam*. Establezca el miembro **lpszText** para que apunte al búfer para recibir el texto de la herramienta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTM \_ GETTEXTW** (Unicode) y **TTM \_ gettexta** (ANSI)<br/>                   |



 

 





