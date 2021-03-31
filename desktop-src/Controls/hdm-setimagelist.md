---
title: Mensaje de HDM_SETIMAGELIST (commctrl. h)
description: Asigna una lista de imágenes a un control de encabezado existente. Puede enviar este mensaje explícitamente o utilizar la \_ macro header SetImageList o header \_ SetStateImageList.
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- HDM_SETIMAGELIST controles de mensajes de Windows
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
ms.openlocfilehash: 17fe21d64b141cf27d32e00fac0ce78228421518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996333"
---
# <a name="hdm_setimagelist-message"></a>HDM \_ SETIMAGELIST

Asigna una lista de imágenes a un control de encabezado existente. Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) o [**Header \_ SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) .

## <a name="parameters"></a>Parámetros

<dl> <dt>*wParam*</dt> <dd>Uno de los siguientes valores:

| Valor                                                                                                                                                      | Significado                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ normal**</dt> </dl> | Indica que se trata de una lista de imágenes normal.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**Estado de HDSIL \_**</dt> </dl>    | Indica que se trata de una lista de imágenes de estado.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de una lista de imágenes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de la lista de imágenes asociada previamente al control. Devuelve **null** si se produce un error o si no se estableció ninguna lista de imágenes previamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





