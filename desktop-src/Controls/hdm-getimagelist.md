---
title: Mensaje de HDM_GETIMAGELIST (commctrl. h)
description: Obtiene el identificador de la lista de imágenes que se ha establecido para un control de encabezado existente. Puede enviar este mensaje explícitamente o utilizar la \_ macro header GetImageList o header \_ GetStateImageList.
ms.assetid: 3e1a979c-60c5-4538-bd4d-16238829062e
keywords:
- HDM_GETIMAGELIST controles de mensajes de Windows
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
ms.openlocfilehash: 5e199d603af873f1957d33855ccf5c59a90a4002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802858"
---
# <a name="hdm_getimagelist-message"></a>HDM \_ GETIMAGELIST

Obtiene el identificador de la lista de imágenes que se ha establecido para un control de encabezado existente. Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) o [**Header \_ GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) .

## <a name="parameters"></a>Parámetros

<dl> <dt>*wParam*</dt> <dd>Uno de los siguientes valores:

| Valor                                                                                                                                                      | Significado                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ normal**</dt> </dl> | Indica que se trata de una lista de imágenes normal.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**Estado de HDSIL \_**</dt> </dl>    | Indica que se trata de una lista de imágenes de estado.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un identificador para el conjunto de lista de imágenes para el control de encabezado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





