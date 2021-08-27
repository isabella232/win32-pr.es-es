---
title: EM_SETWORDBREAKPROC mensaje (Winuser.h)
description: Reemplaza la función wordwrap predeterminada de un control de edición por una función wordwrap definida por la aplicación. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: e5029b75-5f35-43a5-876d-24e81605bb49
keywords:
- EM_SETWORDBREAKPROC controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90617545fab7c8c5cf75babd98e9d6ef85c5713778c52a6a00966a131d0a0581
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048025"
---
# <a name="em_setwordbreakproc-message"></a>Mensaje \_ EM SETWORDBREAKPROC

Reemplaza la función wordwrap predeterminada de un control de edición por una función wordwrap definida por la aplicación. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Dirección de la función wordwrap definida por la aplicación. Para obtener más información sobre las líneas de separación, vea la descripción de la función de devolución de [*llamada EditWordBreakProc.*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

Una función wordwrap examina un búfer de texto que contiene el texto que se va a enviar a la pantalla, buscando la primera palabra que no cabe en la línea de pantalla actual. La función Wordwrap coloca esta palabra al principio de la línea siguiente en la pantalla.

Una función wordwrap define el punto en el que el sistema debe interrumpir una línea de texto para los controles de edición multilínea, normalmente en un carácter de espacio que separa dos palabras. Un control de edición multilínea o de una sola línea podría llamar a esta función cuando el usuario presiona las teclas de dirección en combinación con la tecla CTRL para mover el carácter de diálogo a la palabra siguiente o a la palabra anterior. La función wordwrap predeterminada interrumpe una línea de texto en un carácter de espacio. La función definida por la aplicación puede definir el ajuste de word para que se produzca en un guion o en un carácter distinto del carácter de espacio.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[**EM \_ FMTLINES**](em-fmtlines.md)
</dt> <dt>

[**EM \_ GETWORDBREAKPROC**](em-getwordbreakproc.md)
</dt> </dl>

 

