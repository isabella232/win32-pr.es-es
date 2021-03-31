---
title: Mensaje de ACM_ISPLAYING (commctrl. h)
description: Comprueba si se está reproduciendo un Audio-Video clip intercalado (AVI). Puede enviar este mensaje explícitamente o utilizar la macro Animate \_ IsPlaying.
ms.assetid: ebb0c92a-99d2-49c1-9de1-8bdbd032be3a
keywords:
- ACM_ISPLAYING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- ACM_ISPLAYING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f663872ce02b9520e3e033cb5bc5a3da12bb3c3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079081"
---
# <a name="acm_isplaying-message"></a>\_Mensaje ISPLAYING de ACM

Comprueba si se está reproduciendo un Audio-Video clip intercalado (AVI). Puede enviar este mensaje explícitamente o utilizar la macro [**Animate \_ IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





