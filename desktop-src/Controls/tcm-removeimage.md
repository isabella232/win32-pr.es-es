---
title: TCM_REMOVEIMAGE mensaje (Commctrl.h)
description: Quita una imagen de la lista de imágenes de un control de pestaña. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ RemoveImage.
ms.assetid: f2761338-0afa-47d8-9d9c-1d5a4a7f7bcf
keywords:
- TCM_REMOVEIMAGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_REMOVEIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d2305386f948e1dc4522124708b31ca360203ba9723241c99262fcdb5d2b20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104845"
---
# <a name="tcm_removeimage-message"></a>Mensaje \_ REMOVEIMAGE de TCM

Quita una imagen de la lista de imágenes de un control de pestaña. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ RemoveImage.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la imagen que se quitará.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El control de pestaña actualiza el índice de imagen de cada pestaña, por lo que cada pestaña permanece asociada a la misma imagen que antes. Si una pestaña usa la imagen que se va a quitar, la pestaña se establecerá para que no tenga ninguna imagen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





