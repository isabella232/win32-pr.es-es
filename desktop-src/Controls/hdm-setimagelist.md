---
title: HDM_SETIMAGELIST mensaje (Commctrl.h)
description: Asigna una lista de imágenes a un control de encabezado existente. Puede enviar este mensaje explícitamente o usar la macro Header \_ SetImageList o Header \_ SetStateImageList.
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
ms.openlocfilehash: 17fe21d64b141cf27d32e00fac0ce78228421518
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061973"
---
# <a name="hdm_setimagelist-message"></a>Mensaje \_ SETIMAGELIST de HDM

Asigna una lista de imágenes a un control de encabezado existente. Puede enviar este mensaje explícitamente o usar la macro [**Header \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) [**o Header \_ SetStateImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist)

## <a name="parameters"></a>Parámetros

<dl> <dt>*wParam*</dt> <dd>Uno de los siguientes valores:

| Valor                                                                                                                                                      | Significado                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ NORMAL**</dt> </dl> | Indica que se trata de una lista de imágenes normal.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**HDSIL \_ STATE**</dt> </dl>    | Indica que se trata de una lista de imágenes de estado.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de una lista de imágenes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la lista de imágenes previamente asociada al control . Devuelve **NULL en** caso de error o si no se estableció previamente ninguna lista de imágenes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





