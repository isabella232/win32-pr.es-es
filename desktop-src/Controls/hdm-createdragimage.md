---
title: Mensaje de HDM_CREATEDRAGIMAGE (commctrl. h)
description: Crea una versión semitransparente de la imagen de un elemento para su uso como una imagen de arrastre. Puede enviar este mensaje explícitamente o utilizar la \_ macro header CreateDragImage.
ms.assetid: 1b9dc515-d327-4634-a424-cc15a32f0f7c
keywords:
- HDM_CREATEDRAGIMAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9e801ad9771205b5f2e6df8e37bb0a0ad7f0bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079530"
---
# <a name="hdm_createdragimage-message"></a>HDM \_ CREATEDRAGIMAGE

Crea una versión semitransparente de la imagen de un elemento para su uso como una imagen de arrastre. Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento dentro del control de encabezado. La imagen asignada a este elemento es la base de la imagen transparente.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un identificador a una lista de imágenes que contiene la nueva imagen como su único elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





