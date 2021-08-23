---
title: HDM_GETIMAGELIST mensaje (Commctrl.h)
description: Obtiene el identificador de la lista de imágenes que se ha establecido para un control de encabezado existente. Puede enviar este mensaje explícitamente o usar la macro Header \_ GetImageList o Header \_ GetStateImageList.
ms.assetid: 3e1a979c-60c5-4538-bd4d-16238829062e
keywords:
- HDM_GETIMAGELIST controles de Windows mensaje
topic_type:
- apiref
api_name:
- HDM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8149dd4914ceb1835e9e04442492855e9c25340604ed4e4eeb2619c62b88e69f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540915"
---
# <a name="hdm_getimagelist-message"></a>Mensaje \_ GETIMAGELIST de HDM

Obtiene el identificador de la lista de imágenes que se ha establecido para un control de encabezado existente. Puede enviar este mensaje explícitamente o usar la macro [**Header \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) o [**Header \_ GetStateImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist)

## <a name="parameters"></a>Parámetros

<dl> <dt>*wParam*</dt> <dd>Uno de los siguientes valores:

| Valor                                                                                                                                                      | Significado                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ NORMAL**</dt> </dl> | Indica que se trata de una lista de imágenes normal.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**HDSIL \_ STATE**</dt> </dl>    | Indica que se trata de una lista de imágenes de estado.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un identificador al conjunto de lista de imágenes para el control de encabezado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





