---
title: Mensaje de CBEM_SETIMAGELIST (commctrl. h)
description: Establece una lista de imágenes para un control ComboBoxEx.
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- CBEM_SETIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CBEM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33816abe36e2d1e1593e6365061a500d072c155b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997033"
---
# <a name="cbem_setimagelist-message"></a>CBEM \_ SETIMAGELIST

Establece una lista de imágenes para un control ComboBoxEx.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la lista de imágenes que se va a establecer para el control.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de la lista de imágenes asociada previamente al control o devuelve **null** si no se ha establecido previamente ninguna lista de imágenes.

## <a name="remarks"></a>Observaciones

> [!IMPORTANT]
> El alto de las imágenes de la lista de imágenes podría cambiar los requisitos de tamaño del control ComboBoxEx. Se recomienda que cambie el tamaño del control después de enviar este mensaje para asegurarse de que se muestre correctamente.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





