---
title: EM_LINESCROLL mensaje (Winuser.h)
description: Desplaza el texto en un control de edición multilínea.
ms.assetid: 5398082d-f1ef-4a3a-9e5a-83cf286adbf1
keywords:
- EM_LINESCROLL controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_LINESCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6da4adbd789a8d9ae3344a1a49d39c7f5fbe22b7ec1ca51fcc6cead98ea7780
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048645"
---
# <a name="em_linescroll-message"></a>MENSAJE EM \_ LINESCROLL

Desplaza el texto en un control de edición multilínea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Editar controles:** Número de caracteres que se desplazarán horizontalmente.

**Controles de edición enriquecciones:** Este parámetro no se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Número de líneas que se desplazarán verticalmente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se envía a un control de edición multilínea, el valor devuelto es **TRUE.**

Si el mensaje se envía a un control de edición de una sola línea, el valor devuelto es **FALSE.**

## <a name="remarks"></a>Comentarios

El control no se desplaza verticalmente más allá de la última línea de texto del control de edición. Si la línea actual más el número de líneas especificadas por el parámetro *lParam* supera el número total de líneas del control de edición, el valor se ajusta para que la última línea del control de edición se desplace hasta la parte superior de la ventana de control de edición.

**Editar controles:** El **mensaje EM \_ LINESCROLL** desplaza el texto vertical u horizontalmente en un control de edición multilínea. El **mensaje EM \_ LINESCROLL** se puede usar para desplazarse horizontalmente más allá del último carácter de cualquier línea.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. El **mensaje EM \_ LINESCROLL** desplaza el texto verticalmente en un control de edición multilínea. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

 





