---
title: TCM_SETIMAGELIST mensaje (Commctrl.h)
description: Asigna una lista de imágenes a un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetImageList.
ms.assetid: b457c73c-4c38-4bc5-af5d-12bbd24504a6
keywords:
- TCM_SETIMAGELIST controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59172c677998e816b295939c14effe45ff8aa961
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166210"
---
# <a name="tcm_setimagelist-message"></a>Mensaje \_ SETIMAGELIST de TCM

Asigna una lista de imágenes a un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la lista de imágenes que se asignará al control de pestaña.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la lista de imágenes anterior o **NULL** si no hay ninguna lista de imágenes anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





