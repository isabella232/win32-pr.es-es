---
title: Mensaje de TTM_ENUMTOOLS (commctrl. h)
description: Recupera la información que mantiene un control ToolTip sobre la herramienta actual \ 8212; es decir, la herramienta para la que la información sobre herramientas está mostrando texto actualmente.
ms.assetid: c470db71-c24c-45f4-b497-e59811017eee
keywords:
- TTM_ENUMTOOLS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_ENUMTOOLS
- TTM_ENUMTOOLSA
- TTM_ENUMTOOLSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad1679f9740539507a57c4cba93319569add0af3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490684"
---
# <a name="ttm_enumtools-message"></a>TTM \_ ENUMTOOLS

Recupera la información que mantiene un control ToolTip sobre la herramienta actual, es decir, la herramienta para la que la información sobre herramientas está mostrando texto actualmente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la herramienta para la que se va a recuperar información.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que recibe información sobre la herramienta. Establezca el miembro **cbSize** de esta estructura en SIZEOF (TOOLINFO) antes de enviar este mensaje. Asigne un búfer. Establezca el miembro **lpszText** para que apunte al búfer para recibir el texto de la herramienta. No hay ninguna manera de determinar el tamaño de búfer necesario. Sin embargo, el texto de la herramienta, tal como se devuelve en el miembro **lpszText** de la estructura **TOOLINFO** , tiene una longitud máxima de 80 **TCHARs**, incluido el carácter **nulo** final. Si el texto supera esta longitud, se trunca.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si se enumera cualquier herramienta o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

**Advertencia de seguridad:** El uso de este mensaje podría poner en peligro la seguridad del programa. Este mensaje no proporciona una manera para que el receptor del mensaje conozca el tamaño del búfer o para especificar el tamaño del búfer. Debe revisar las [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md) antes de continuar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTM \_ ENUMTOOLSW** (Unicode) y **TTM \_ ENUMTOOLSA** (ANSI)<br/>               |



 

 





