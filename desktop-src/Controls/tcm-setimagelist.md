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
ms.openlocfilehash: e3fee54072091f177d1600f81f659b69a2713d4c689c6e1a2e0b05f74777e01e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104865"
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
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





