---
title: EM_GETFIRSTVISIBLELINE mensaje (Winuser.h)
description: Obtiene el índice de base cero de la línea visible superior en un control de edición de varias líneas. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
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
ms.openlocfilehash: 2bb759be166b69b3cfa488e9e23d61d9e0ec42d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167946"
---
# <a name="em_getfirstvisibleline-message"></a>Mensaje \_ EM GETFIRSTVISIBLELINE

Obtiene el índice de base cero de la línea visible superior en un control de edición de varias líneas. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

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

**Controles de edición enriquecciones:** En el caso de los controles de edición enriquecidos de una sola línea, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

El número de líneas y la longitud de las líneas de un control de edición dependen del ancho del control y de la configuración de wordwrap actual.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

 





