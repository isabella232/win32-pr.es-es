---
title: RB_SETBANDINFO mensaje (Commctrl.h)
description: Establece las características de una banda existente en un control rebar.
ms.assetid: 00021c35-612d-4278-b10c-6e9f1f45a543
keywords:
- RB_SETBANDINFO controles de Windows mensaje
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
ms.openlocfilehash: aee89d91bc65556179d14c7e86a69a9e6399223f38bb1bcc44f746d7cd8f8a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798475"
---
# <a name="rb_setbandinfo-message"></a>Mensaje \_ SETBANDINFO de RB

Establece las características de una banda existente en un control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la banda para recibir la nueva configuración.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) que define la banda que se va a modificar y la nueva configuración. Antes de enviar este mensaje, debe establecer el **miembro cbSize** de esta estructura en la **estructura sizeof**(REBARBANDINFO). Además, debe establecer el miembro **cch** de la estructura **REBARBANDINFO** en el tamaño del búfer **lpText** cuando se especifica RBBIM \_ TEXT.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **RB \_ SETBANDINFOW** (Unicode) y **RB \_ SETBANDINFOA** (ANSI)<br/>             |



 

 





