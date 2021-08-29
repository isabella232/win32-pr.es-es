---
title: TTM_ENUMTOOLS mensaje (Commctrl.h)
description: Recupera la información que un control de información sobre herramientas mantiene sobre la herramienta actual \ 8212; es decir, la herramienta para la que la información sobre herramientas muestra texto actualmente.
ms.assetid: c470db71-c24c-45f4-b497-e59811017eee
keywords:
- TTM_ENUMTOOLS controles de Windows mensaje
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
ms.openlocfilehash: e7534169bb0808daa63e835d3a46bf4ab31c059b63267727d5c4dbf43f28864d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769485"
---
# <a name="ttm_enumtools-message"></a>Mensaje DE \_ ENUMTOOLS de TTM

Recupera la información que un control de información sobre herramientas mantiene sobre la herramienta actual, es decir, la herramienta para la que la información sobre herramientas muestra texto actualmente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la herramienta para la que se va a recuperar información.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que recibe información sobre la herramienta. Establezca el **miembro cbSize** de esta estructura en sizeof(TOOLINFO) antes de enviar este mensaje. Asigne un búfer. Establezca el **miembro lpszText** para que apunte al búfer para recibir el texto de la herramienta. No hay ninguna manera de determinar el tamaño de búfer necesario. Sin embargo, el texto de la herramienta, tal como se devuelve en el miembro **lpszText** de la estructura **TOOLINFO,** tiene una longitud máxima de 80 **TCHAR,** incluido el **valor NULL** final. Si el texto supera esta longitud, se trunca.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **FALSE** tanto si se enumeró una herramienta como si no.

## <a name="remarks"></a>Comentarios

**Advertencia de seguridad:** El uso de este mensaje puede poner en peligro la seguridad del programa. Este mensaje no proporciona una manera de que el receptor del mensaje conozca el tamaño del búfer o especifique el tamaño del búfer. Debe revisar las [Consideraciones de seguridad: Controles de Windows Microsoft](sec-comctls.md) antes de continuar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTM \_ ENUMTOOLSW** (Unicode) y **TTM \_ ENUMTOOLSA** (ANSI)<br/>               |



 

 





