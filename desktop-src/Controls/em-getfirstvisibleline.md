---
title: EM_GETFIRSTVISIBLELINE mensaje (Winuser.h)
description: Obtiene el índice de base cero de la línea visible superior en un control de edición multilínea. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: 022838d2-7948-4c5a-92ca-655822c4f672
keywords:
- EM_GETFIRSTVISIBLELINE controles de Windows mensaje
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
ms.openlocfilehash: 11eb93c1c7dcce7f502945df4e063b22c29514bc79fe7310875e9de055e1d745
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049215"
---
# <a name="em_getfirstvisibleline-message"></a>Mensaje \_ EM GETFIRSTVISIBLELINE

Obtiene el índice de base cero de la línea visible superior en un control de edición multilínea. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

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

El valor devuelto es el índice de base cero de la línea visible superior en un control de edición multilínea.

**Editar controles:** Para los controles de edición de una sola línea, el valor devuelto es el índice de base cero del primer carácter visible.

**Controles de edición enriquecciones:** En el caso de los controles de edición enriquecciones de una sola línea, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

El número de líneas y la longitud de las líneas de un control de edición dependen del ancho del control y de la configuración de wordwrap actual.

**Edición enriqueceda:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

 





