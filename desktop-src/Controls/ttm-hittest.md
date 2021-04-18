---
title: Mensaje de TTM_HITTEST (commctrl. h)
description: Comprueba un punto para determinar si está dentro del rectángulo delimitador de la herramienta especificada y, si es así, recupera información sobre la herramienta.
ms.assetid: d4dcc29b-c64c-41b8-a153-300df68ecdf5
keywords:
- TTM_HITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_HITTEST
- TTM_HITTESTA
- TTM_HITTESTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b515ccb5c283b66760f24c02749368e424e6fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490673"
---
# <a name="ttm_hittest-message"></a>TTM \_ mensaje HITTEST

Comprueba un punto para determinar si está dentro del rectángulo delimitador de la herramienta especificada y, si es así, recupera información sobre la herramienta.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) . Al enviar el mensaje, el miembro **hWnd** debe especificar el identificador de una herramienta y el miembro **PT** debe especificar las coordenadas de un punto. Si el valor devuelto es **true**, el miembro de **ti** (una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ) recibe información sobre la herramienta que ocupa el punto. El miembro **cbSize** de la estructura de **ti** se debe rellenar antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si la herramienta ocupa el punto especificado o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje se debe enviar cuando la herramienta tiene establecida la \_ marca de seguimiento ttf. Para obtener más información sobre esta marca, vea [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa). TTM \_ HITTEST producirá un error si \_ no se establece la pista ttf, independientemente de si el punto de acierto está en el rectángulo de herramientas o no.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTM \_ HITTESTW** (Unicode) y **TTM \_ HITTESTA** (ANSI)<br/>                   |



 

 





