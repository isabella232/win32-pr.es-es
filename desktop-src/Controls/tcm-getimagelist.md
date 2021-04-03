---
title: Mensaje de TCM_GETIMAGELIST (commctrl. h)
description: Recupera la lista de imágenes asociada a un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetImageList.
ms.assetid: 86a0d8c7-ff3d-4e16-994e-4c72d1e62e9f
keywords:
- TCM_GETIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c4d471ef4d072e4305507f4f5ebc4a8f2745ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905549"
---
# <a name="tcm_getimagelist-message"></a>\_Mensaje GETIMAGELIST de TCM

Recupera la lista de imágenes asociada a un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de la lista de imágenes si se realiza correctamente, o **null** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





