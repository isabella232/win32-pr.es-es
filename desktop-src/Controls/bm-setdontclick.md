---
title: BM_SETDONTCLICK mensaje (Winuser.h)
description: Establece una marca en un botón de radio que controla la generación de mensajes CLICKED de BN \_ cuando el botón recibe el foco.
ms.assetid: 91d98bce-abea-4afc-a995-0f426ba7a518
keywords:
- BM_SETDONTCLICK controles de Windows mensaje
topic_type:
- apiref
api_name:
- BM_SETDONTCLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a118b0e9ed3e1ea797cdd0b690aee0fe3c4cc067b72990d884fdd121fcb80c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921245"
---
# <a name="bm_setdontclick-message"></a>Mensaje \_ BM SETDONTCLICK

Establece una marca en un botón de radio que controla la generación de mensajes [ \_ CLICKED](bn-clicked.md) de BN cuando el botón recibe el foco.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Valor **BOOL** que especifica el estado. **TRUE** para establecer la marca; de lo **contrario, FALSE.**

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa. Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

 





