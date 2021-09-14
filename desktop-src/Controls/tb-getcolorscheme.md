---
title: TB_GETCOLORSCHEME mensaje (Commctrl.h)
description: Recupera la información de combinación de colores del control de barra de herramientas.
ms.assetid: af172631-309e-4181-a690-05946cd6e143
keywords:
- TB_GETCOLORSCHEME controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61344439ae8bc2b3a9ecd47472174577d652aa96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166837"
---
# <a name="tb_getcolorscheme-message"></a>Mensaje \_ GETCOLORSCHEME de TB

Recupera la información de combinación de colores del control de barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) que recibirá la información de la combinación de colores. Debe establecer el **miembro cbSize** de esta estructura en **sizeof**(COLORSCHEME) antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TB \_ SETCOLORSCHEME**](tb-setcolorscheme.md)
</dt> </dl>

 

 





