---
title: Mensaje de TVM_SETIMAGELIST (commctrl. h)
description: Establece la lista de imágenes normal o de estado de un control de vista de árbol y vuelve a dibujar el control mediante las nuevas imágenes. Puede enviar este mensaje explícitamente o mediante la \_ macro SetImageList de TreeView.
ms.assetid: 1a7bf2f8-c7db-44a8-b234-0ffc498e9000
keywords:
- TVM_SETIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f308cb8a56b2e74a5703af144bac03c271efc95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802317"
---
# <a name="tvm_setimagelist-message"></a>\_Mensaje de SETIMAGELIST TVM

Establece la lista de imágenes normal o de estado de un control de vista de árbol y vuelve a dibujar el control mediante las nuevas imágenes. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetImageList de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de lista de imágenes que se va a establecer. Este parámetro puede ser uno de los siguientes valores:



| Value                                                                                                                                                      | Significado                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <dt>**TVSIL \_ normal**</dt> </dl> | Indica la lista de imágenes normal, que contiene imágenes seleccionadas, no seleccionadas y superpuestas para los elementos de un control de vista de árbol.<br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <dt>**Estado de TVSIL \_**</dt> </dl>    | Indica la lista de imágenes de estado. Puede usar imágenes de estado para indicar los Estados de los elementos definidos por la aplicación. Se muestra una imagen de estado a la izquierda de la imagen seleccionada o no seleccionada de un elemento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la lista de imágenes. Si *lParam* es **null**, el mensaje quita la lista de imágenes especificada del control de vista de árbol.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de la lista de imágenes anterior, si existe, o **null** en caso contrario.

## <a name="remarks"></a>Observaciones

El control de vista de árbol no destruirá la lista de imágenes especificada con este mensaje. La aplicación debe destruir la lista de imágenes cuando ya no se necesite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ GETIMAGELIST**](tvm-getimagelist.md)
</dt> </dl>

 

 





