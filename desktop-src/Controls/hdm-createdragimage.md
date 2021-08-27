---
title: HDM_CREATEDRAGIMAGE mensaje (Commctrl.h)
description: Crea una versión semitransparente de la imagen de un elemento para usarla como una imagen de arrastre. Puede enviar este mensaje explícitamente o usar la \_ macro Header CreateDragImage.
ms.assetid: 1b9dc515-d327-4634-a424-cc15a32f0f7c
keywords:
- HDM_CREATEDRAGIMAGE controles de Windows mensaje
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
ms.openlocfilehash: 1507f3e72ce75394aaad834fe5c0d876fc579a671ad8f2df00865b2278ad6e32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047235"
---
# <a name="hdm_createdragimage-message"></a>Mensaje \_ CREATEDRAGIMAGE de HDM

Crea una versión semitransparente de la imagen de un elemento para usarla como una imagen de arrastre. Puede enviar este mensaje explícitamente o usar la macro [**\_ Header CreateDragImage.**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage)

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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





