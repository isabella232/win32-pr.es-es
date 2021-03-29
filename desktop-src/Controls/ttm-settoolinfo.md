---
title: Mensaje de TTM_SETTOOLINFO (commctrl. h)
description: Establece la información que mantiene un control ToolTip para una herramienta.
ms.assetid: ba18f651-2e52-46e2-871b-c1760e94ab59
keywords:
- TTM_SETTOOLINFO controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492844"
---
# <a name="ttm_settoolinfo-message"></a>TTM \_ SETTOOLINFO

Establece la información que mantiene un control ToolTip para una herramienta.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que especifica la información que se va a establecer. El miembro **cbSize** de esta estructura debe establecerse antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Algunas propiedades internas de una herramienta se establecen cuando se crea la herramienta y no se vuelven a calcular cuando se envía un mensaje **\_ SETTOOLINFO de TTM** . Si simplemente asigna valores a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) y lo pasa al control ToolTip con un mensaje **TTM \_ SETTOOLINFO** , estas propiedades se pueden perder. En su lugar, la aplicación debe solicitar primero la estructura **TOOLINFO** actual de la herramienta mediante el envío del mensaje de control de información sobre herramientas [**TTM \_ GETTOOLINFO**](ttm-gettoolinfo.md) . A continuación, modifique los miembros de esta estructura según sea necesario y páselo de vuelta al control ToolTip con **TTM \_ SETTOOLINFO**.

Al llamar a **TTM \_ SETTOOLINFO**, la cadena a la que apunta el miembro **LpszText** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) no debe superar los 80 **TCHARs** de longitud, incluido el **valor null** final.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTM \_ SETTOOLINFOW** (Unicode) y **TTM \_ SETTOOLINFOA** (ANSI)<br/>           |



 

 





