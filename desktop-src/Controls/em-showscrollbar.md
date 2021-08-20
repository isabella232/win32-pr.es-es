---
title: EM_SHOWSCROLLBAR mensaje (Richedit.h)
description: Muestra u oculta una de las barras de desplazamiento en la ventana host de un control de edición enriquecido.
ms.assetid: 0a6ec010-4870-4faf-9dc2-1da961dc8194
keywords:
- EM_SHOWSCROLLBAR controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SHOWSCROLLBAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc3988ced825fed457549fc9f662a418295de7df6085f04c3e71255ca4ad54c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831146"
---
# <a name="em_showscrollbar-message"></a>MENSAJE \_ DE EM SHOWSCROLLBAR

Muestra u oculta una de las barras de desplazamiento en la ventana host de un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identifica la barra de desplazamiento que se va a mostrar: horizontal o vertical. Este parámetro debe ser **SB \_ VERT** o **SB \_ HORZ.**

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica si se debe mostrar la barra de desplazamiento u ocultarla. Especifique **TRUE** para mostrar la barra de desplazamiento y **FALSE** para ocultarla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este método solo es válido cuando el control está activo en su lugar. Las llamadas realizadas mientras el control está inactivo pueden producir un error.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ GETSCROLLPOS**](em-getscrollpos.md)
</dt> <dt>

[**EM \_ SETSCROLLPOS**](em-setscrollpos.md)
</dt> </dl>

 

 





