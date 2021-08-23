---
title: HDM_SETIMAGELIST mensaje (Commctrl.h)
description: Asigna una lista de imágenes a un control de encabezado existente. Puede enviar este mensaje explícitamente o usar la macro \_ Header SetImageList o Header \_ SetStateImageList.
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- HDM_SETIMAGELIST controles de Windows mensaje
topic_type:
- apiref
api_name:
- HDM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2034a6880721914961b3bd75907df2e7b4e53360ccb3b10162f238068d85031d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435815"
---
# <a name="hdm_setimagelist-message"></a>Mensaje \_ SETIMAGELIST de HDM

Asigna una lista de imágenes a un control de encabezado existente. Puede enviar este mensaje explícitamente o usar la macro [**\_ Header SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) [**o Header \_ SetStateImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist)

## <a name="parameters"></a>Parámetros

<dl> <dt>*wParam*</dt> <dd>Uno de los siguientes valores:

| Valor                                                                                                                                                      | Significado                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ NORMAL**</dt> </dl> | Indica que se trata de una lista de imágenes normal.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**ESTADO DE \_ HDSIL**</dt> </dl>    | Indica que se trata de una lista de imágenes de estado.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de una lista de imágenes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la lista de imágenes previamente asociada al control . Devuelve **NULL en** caso de error o si no se estableció previamente ninguna lista de imágenes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





