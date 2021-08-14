---
title: TVM_CREATEDRAGIMAGE mensaje (Commctrl.h)
description: Crea un mapa de bits de arrastre para el elemento especificado en un control de vista de árbol.
ms.assetid: fbe97921-c9d3-473c-933c-d6bc0599e24d
keywords:
- TVM_CREATEDRAGIMAGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a18a00b2225749b30b8dcd9a928fd73e3ffabcfd4a4f9512cd2332d98cc08a79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408665"
---
# <a name="tvm_createdragimage-message"></a>Mensaje DE TVM \_ CREATEDRAGIMAGE

Crea un mapa de bits de arrastre para el elemento especificado en un control de vista de árbol. El mensaje también crea una lista de imágenes para el mapa de bits y agrega el mapa de bits a la lista de imágenes. Una aplicación puede mostrar la imagen al arrastrar el elemento mediante las funciones de lista de imágenes. Puede enviar este mensaje explícitamente o mediante la macro [**\_ TreeView CreateDragImage.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del elemento que recibe el nuevo mapa de bits de arrastre.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la lista de imágenes a la que se agregó el mapa de bits de arrastre si se realiza correctamente o NULL en **caso** contrario.

## <a name="remarks"></a>Comentarios

Si crea un control de vista de árbol sin una lista de imágenes asociada, no puede usar el mensaje **\_ CREATEDRAGIMAGE** de TVM para crear la imagen que se mostrará durante una operación de arrastre. Debe implementar su propio método para crear un cursor de arrastre.

La aplicación es responsable de destruir la lista de imágenes cuando ya no se necesite.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





