---
title: TCM_REMOVEIMAGE mensaje (Commctrl.h)
description: Quita una imagen de la lista de imágenes de un control de pestaña. Puede enviar este mensaje explícitamente o mediante la macro \_ TabCtrl RemoveImage.
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
ms.openlocfilehash: 6cbc51aa0efed847e39e735443c0d42e288bbaab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166226"
---
# <a name="tcm_removeimage-message"></a>Mensaje \_ REMOVEIMAGE de TCM

Quita una imagen de la lista de imágenes de un control de pestaña. Puede enviar este mensaje explícitamente o mediante la macro [**\_ TabCtrl RemoveImage.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage)

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

## <a name="remarks"></a>Observaciones

El control de pestaña actualiza el índice de imagen de cada pestaña, por lo que cada pestaña permanece asociada a la misma imagen que antes. Si una pestaña usa la imagen que se va a quitar, la pestaña se establecerá para que no tenga ninguna imagen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





