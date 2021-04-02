---
title: Mensaje de EM_GETTHUMB (Winuser. h)
description: Obtiene la posición del cuadro de desplazamiento (Thumb) en la barra de desplazamiento vertical de un control de edición multilínea. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 04bd0102-1652-405b-8c42-50e138abaf75
keywords:
- EM_GETTHUMB controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETTHUMB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6689c530794e11897f1f88a7d5864058d53aa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150763"
---
# <a name="em_getthumb-message"></a>\_Mensaje GETTHUMB em

Obtiene la posición del cuadro de desplazamiento (Thumb) en la barra de desplazamiento vertical de un control de edición multilínea. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es la posición del cuadro de desplazamiento.

## <a name="remarks"></a>Observaciones

**Edición enriquecida:** Compatible con Microsoft Rich Edit 2,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



 

 





