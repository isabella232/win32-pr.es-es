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
ms.openlocfilehash: 0b4ed278ea31dfa156dcc8a64afdb98a2ae3b938
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166637"
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

## <a name="remarks"></a>Observaciones

El control de barra de herramientas usa la información de combinación de colores al dibujar los elementos 3D del control.

Cuando los estilos visuales están habilitados, este mensaje no tiene ningún efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TB \_ GETCOLORSCHEME**](tb-getcolorscheme.md)
</dt> </dl>

 

 





