---
title: Mensaje de TVM_CREATEDRAGIMAGE (commctrl. h)
description: Crea un mapa de bits de arrastre para el elemento especificado en un control de vista de árbol.
ms.assetid: fbe97921-c9d3-473c-933c-d6bc0599e24d
keywords:
- TVM_CREATEDRAGIMAGE controles de mensajes de Windows
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
ms.openlocfilehash: 189b37affc6a4382541faea13199cacfcb9b7df5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150360"
---
# <a name="tvm_createdragimage-message"></a>\_Mensaje de CREATEDRAGIMAGE TVM

Crea un mapa de bits de arrastre para el elemento especificado en un control de vista de árbol. El mensaje también crea una lista de imágenes para el mapa de bits y agrega el mapa de bits a la lista de imágenes. Una aplicación puede mostrar la imagen al arrastrar el elemento mediante las funciones de la lista de imágenes. Puede enviar este mensaje explícitamente o mediante la macro [**\_ CreateDragImage de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del elemento que recibe el nuevo mapa de bits de arrastre.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de la lista de imágenes a la que se agregó el mapa de bits de arrastre si se realiza correctamente, o **null** en caso contrario.

## <a name="remarks"></a>Observaciones

Si crea un control de vista de árbol sin una lista de imágenes asociada, no puede usar el mensaje **TVM \_ CREATEDRAGIMAGE** para crear la imagen que se va a mostrar durante una operación de arrastre. Debe implementar su propio método para crear un cursor de arrastre.

La aplicación es responsable de destruir la lista de imágenes cuando ya no se necesita.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





