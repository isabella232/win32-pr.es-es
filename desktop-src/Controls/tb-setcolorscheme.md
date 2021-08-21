---
title: TB_SETCOLORSCHEME mensaje (Commctrl.h)
description: Establece la información de combinación de colores para el control de barra de herramientas.
ms.assetid: 96cf6464-b760-46af-910f-984e41dbfca5
keywords:
- TB_SETCOLORSCHEME controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58c6a07c186fd3f5a521719ba0f75f8e468c3868d8ebfaa0595679d48b45089f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167505"
---
# <a name="tb_setcolorscheme-message"></a>Mensaje \_ SETCOLORSCHEME de TB

Establece la información de combinación de colores para el control de barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) que contiene la información de combinación de colores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="remarks"></a>Comentarios

El control de barra de herramientas usa la información de combinación de colores al dibujar los elementos 3D del control.

Cuando los estilos visuales están habilitados, este mensaje no tiene ningún efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TB \_ GETCOLORSCHEME**](tb-getcolorscheme.md)
</dt> </dl>

 

 





