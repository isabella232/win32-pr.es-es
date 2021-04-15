---
title: Mensaje de EM_GETFIRSTVISIBLELINE (Winuser. h)
description: Obtiene el índice de base cero de la línea visible superior de un control de edición multilínea. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 022838d2-7948-4c5a-92ca-655822c4f672
keywords:
- EM_GETFIRSTVISIBLELINE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETFIRSTVISIBLELINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb759be166b69b3cfa488e9e23d61d9e0ec42d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534689"
---
# <a name="em_getfirstvisibleline-message"></a>\_Mensaje GETFIRSTVISIBLELINE em

Obtiene el índice de base cero de la línea visible superior de un control de edición multilínea. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

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

El valor devuelto es el índice de base cero de la línea visible superior en un control de edición multilínea.

**Controles de edición:** En el caso de los controles de edición de una sola línea, el valor devuelto es el índice de base cero del primer carácter visible.

**Controles Rich Edit:** En el caso de los controles de edición enriquecida de una sola línea, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

El número de líneas y la longitud de las líneas en un control de edición dependen del ancho del control y del valor de WordWrap actual.

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



 

 





