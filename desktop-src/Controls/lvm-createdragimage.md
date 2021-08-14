---
title: LVM_CREATEDRAGIMAGE mensaje (Commctrl.h)
description: Crea una lista de imágenes de arrastre para el elemento especificado. Puede enviar este mensaje explícitamente o mediante la macro \_ CreateDragImage de ListView.
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- LVM_CREATEDRAGIMAGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d551dfa7b14ecff8c9fd1efe015e173403c1b5981f294a18b3180a42cc03de63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412003"
---
# <a name="lvm_createdragimage-message"></a>Mensaje LVM \_ CREATEDRAGIMAGE

Crea una lista de imágenes de arrastre para el elemento especificado. Puede enviar este mensaje explícitamente o mediante la macro [**\_ CreateDragImage de ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura POINT**](/previous-versions//dd162805(v=vs.85)) que recibe la ubicación inicial de la esquina superior izquierda de la imagen, en coordenadas de vista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la lista de imágenes de arrastre si se realiza correctamente o **NULL** en caso contrario.

## <a name="remarks"></a>Comentarios

La aplicación es responsable de destruir la lista de imágenes cuando ya no sea necesaria.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

