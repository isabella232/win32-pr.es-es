---
title: TTM_HITTEST mensaje (Commctrl.h)
description: Prueba un punto para determinar si está dentro del rectángulo delimitador de la herramienta especificada y, si es así, recupera información sobre la herramienta.
ms.assetid: d4dcc29b-c64c-41b8-a153-300df68ecdf5
keywords:
- TTM_HITTEST controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165886"
---
# <a name="ttm_hittest-message"></a>Mensaje \_ HITTEST de TTM

Prueba un punto para determinar si está dentro del rectángulo delimitador de la herramienta especificada y, si es así, recupera información sobre la herramienta.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TTHITTESTINFO.**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) Al enviar el mensaje, el **miembro hwnd** debe especificar el identificador a una herramienta y el **miembro pt** debe especificar las coordenadas de un punto. Si el valor devuelto es **TRUE,** el **miembro ti** (una [**estructura TOOLINFO)**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) recibe información sobre la herramienta que ocupa el punto. El **miembro cbSize** de la **estructura ti** debe rellenarse antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si la herramienta ocupa el punto especificado o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje se debe enviar cuando la herramienta tiene establecida la marca \_ TTF TRACK. Para obtener más información sobre esta marca, vea [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa). SE producirá un error en EL HITTEST de TTM si no se establece TTF TRACK, independientemente de si el punto de acceso está en el rectángulo de \_ \_ herramientas o no.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTM \_ HITTESTW** (Unicode) y **TTM \_ HITTESTA** (ANSI)<br/>                   |



 

 





