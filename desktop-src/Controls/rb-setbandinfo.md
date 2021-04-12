---
title: Mensaje de RB_SETBANDINFO (commctrl. h)
description: Establece las características de una banda existente en un control rebar.
ms.assetid: 00021c35-612d-4278-b10c-6e9f1f45a543
keywords:
- RB_SETBANDINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_SETBANDINFO
- RB_SETBANDINFOA
- RB_SETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e81377a40f8b6054f5d8cfae16837621b77b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491758"
---
# <a name="rb_setbandinfo-message"></a>Mensaje de SETBANDINFO de RB \_

Establece las características de una banda existente en un control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la banda que va a recibir la nueva configuración.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) que define la banda que se va a modificar y la nueva configuración. Antes de enviar este mensaje, debe establecer el miembro **cbSize** de esta estructura en la estructura **sizeof**(REBARBANDINFO). Además, debe establecer el miembro **CCH** de la estructura **REBARBANDINFO** en el tamaño del búfer **lpText** cuando \_ se especifica RBBIM Text.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **RB \_ SETBANDINFOW** (Unicode) y **RB \_ SETBANDINFOA** (ANSI)<br/>             |



 

 





