---
title: RB_GETBANDINFO mensaje (Commctrl.h)
description: Recupera información sobre una banda especificada en un control rebar.
ms.assetid: c2a76c91-7d44-4278-823d-bd263520e7a8
keywords:
- RB_GETBANDINFO controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_GETBANDINFO
- RB_GETBANDINFOA
- RB_GETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b0ae509699c23ad24b9b97451178f4711ab52176a9c15aeef757bab85c861c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409446"
---
# <a name="rb_getbandinfo-message"></a>Mensaje \_ GETBANDINFO de RB

Recupera información sobre una banda especificada en un control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la banda para la que se recuperará la información.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) que recibirá la información de banda solicitada. Antes de enviar este mensaje, debe establecer el miembro **cbSize** de esta estructura en el tamaño de la estructura **REBARBANDINFO** y establecer el miembro **fMask** en los elementos que desea recuperar. Además, debe establecer el miembro **cch** de la estructura **REBARBANDINFO** en el tamaño del búfer **lpText** cuando se especifica RBBIM \_ TEXT.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **RB \_ GETBANDINFOW** (Unicode) y **RB \_ GETBANDINFOA** (ANSI)<br/>             |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RB \_ SETBANDINFO**](rb-setbandinfo.md)
</dt> </dl>

 

 





