---
title: EM_REPLACESEL mensaje (Winuser.h)
description: Reemplaza el texto seleccionado en un control de edición o un control de edición enriquecido por el texto especificado.
ms.assetid: 525e6f5a-f52f-4bab-bc76-caa484729897
keywords:
- EM_REPLACESEL controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_REPLACESEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 478550432aa8c03a081e8de214cdd7e8337a46eca2676a0531b177a81ff20a54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831186"
---
# <a name="em_replacesel-message"></a>Mensaje \_ DE EM REPLACESEL

Reemplaza el texto seleccionado en un control de edición o un control de edición enriquecido por el texto especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si la operación de reemplazo se puede deshacer. Si es **TRUE,** la operación se puede deshacer. Si es **FALSE,** la operación no se puede deshacer.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene el texto de reemplazo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

Use el **mensaje EM \_ REPLACESEL** para reemplazar solo una parte del texto en un control de edición. Para reemplazar todo el texto, use el [**mensaje \_ SETTEXT de WM.**](/windows/desktop/winmsg/wm-settext)

Si no hay ninguna selección, el texto de reemplazo se inserta en el símbolo de inserción.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

En un control de edición enriquecido, el texto de reemplazo toma el formato del carácter en el carácter de careta o, si hay una selección, del primer carácter de la selección.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

