---
title: Mensaje de EM_LINESCROLL (Winuser. h)
description: Desplaza el texto en un control de edición multilínea.
ms.assetid: 5398082d-f1ef-4a3a-9e5a-83cf286adbf1
keywords:
- EM_LINESCROLL controles de mensajes de Windows
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
ms.openlocfilehash: 646e225ef269ccddca2cdc29caf635d94c1671e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079567"
---
# <a name="em_linescroll-message"></a>\_Mensaje LINESCROLL em

Desplaza el texto en un control de edición multilínea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Controles de edición:** Número de caracteres que se va a desplazar horizontalmente.

**Controles Rich Edit:** Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Número de líneas que se va a desplazar verticalmente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se envía a un control de edición de varias líneas, el valor devuelto es **true**.

Si el mensaje se envía a un control de edición de una sola línea, el valor devuelto es **false**.

## <a name="remarks"></a>Observaciones

El control no se desplaza verticalmente más allá de la última línea de texto del control de edición. Si la línea actual más el número de líneas especificadas por el parámetro *lParam* supera el número total de líneas en el control de edición, el valor se ajusta de modo que la última línea del control de edición se desplaza a la parte superior de la ventana Editar control.

**Controles de edición:** El **mensaje \_ LINESCROLL em** desplaza el texto vertical u horizontalmente en un control de edición multilínea. El **mensaje \_ LINESCROLL em** se puede usar para desplazarse horizontalmente más allá del último carácter de cualquier línea.

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. El **mensaje \_ LINESCROLL em** desplaza el texto verticalmente en un control de edición multilínea. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



 

 





