---
title: TTM_SETTOOLINFO mensaje (Commctrl.h)
description: Establece la información que un control de información sobre herramientas mantiene para una herramienta.
ms.assetid: ba18f651-2e52-46e2-871b-c1760e94ab59
keywords:
- TTM_SETTOOLINFO controles de Windows mensaje
topic_type:
- apiref
api_name:
- TTM_SETTOOLINFO
- TTM_SETTOOLINFOA
- TTM_SETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327dd853e3304f8233b95c947a890c4f49298cc7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165842"
---
# <a name="ttm_settoolinfo-message"></a>Mensaje \_ SETTOOLINFO de TTM

Establece la información que un control de información sobre herramientas mantiene para una herramienta.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que especifica la información que se debe establecer. El **miembro cbSize** de esta estructura debe establecerse antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Algunas propiedades internas de una herramienta se establecen cuando se crea la herramienta y no se vuelve a compilar cuando se envía un mensaje **\_ SETTOOLINFO de TTM.** Si simplemente asigna valores a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) y lo pasa al control de información sobre herramientas con un mensaje **\_ SETTOOLINFO de TTM,** es posible que estas propiedades se pierdan. En su lugar, la aplicación debe solicitar primero la estructura **TOOLINFO** actual de la herramienta enviando al control de información sobre herramientas un [**mensaje \_ GETTOOLINFO de TTM.**](ttm-gettoolinfo.md) A continuación, modifique los miembros de esta estructura según sea necesario y vuelva a pasarlo al control de información sobre herramientas **con EL \_ SETTOOLINFO de TTM.**

Al llamar **a \_ SETTOOLINFO** de TTM, la cadena a la que apunta el miembro **lpszText** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) no debe superar los 80 **TCHAR** de longitud, incluido el valor **NULL** final.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTM \_ SETTOOLINFOW** (Unicode) y **TTM \_ SETTOOLINFOA** (ANSI)<br/>           |



 

 





