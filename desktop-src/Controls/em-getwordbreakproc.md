---
title: EM_GETWORDBREAKPROC mensaje (Winuser.h)
description: Obtiene la dirección de la función wordwrap actual. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: 564b4b1b-913f-4040-bb28-eea50c0c3738
keywords:
- EM_GETWORDBREAKPROC controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb9499492668abac24774b66304ae8a87a2d739
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062178"
---
# <a name="em_getwordbreakproc-message"></a>Mensaje \_ EM GETWORDBREAKPROC

Obtiene la dirección de la función wordwrap actual. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto especifica la dirección de la función Wordwrap definida por la aplicación. El valor devuelto es **NULL si** no existe ninguna función wordwrap.

## <a name="remarks"></a>Observaciones

Una función Wordwrap examina un búfer de texto que contiene el texto que se va a enviar a la pantalla, buscando la primera palabra que no cabe en la línea de presentación actual. La función wordwrap coloca esta palabra al principio de la línea siguiente en la pantalla. Una función wordwrap define el punto en el que el sistema debe interrumpir una línea de texto para los controles de edición multilínea, normalmente en un carácter de espacio que separa dos palabras.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[**EM \_ FMTLINES**](em-fmtlines.md)
</dt> <dt>

[**EM \_ SETWORDBREAKPROC**](em-setwordbreakproc.md)
</dt> </dl>

 

