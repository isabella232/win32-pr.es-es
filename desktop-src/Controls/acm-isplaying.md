---
title: ACM_ISPLAYING mensaje (Commctrl.h)
description: Comprueba si se está Audio-Video clip intercalado (AVI). Puede enviar este mensaje explícitamente o usar la \_ macro Animate IsPlaying.
ms.assetid: ebb0c92a-99d2-49c1-9de1-8bdbd032be3a
keywords:
- ACM_ISPLAYING controles de Windows mensaje
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
ms.openlocfilehash: db85d2b25b0f8498c020a78b3e43cfe48877b0cb0b8b77fe33cbb4caa2a3f311
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079419"
---
# <a name="acm_isplaying-message"></a>Mensaje \_ ISPLAYING de ACM

Comprueba si se está Audio-Video clip intercalado (AVI). Puede enviar este mensaje explícitamente o usar la macro [**Animate \_ IsPlaying.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying)

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

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





