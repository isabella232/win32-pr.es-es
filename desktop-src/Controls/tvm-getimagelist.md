---
title: TVM_GETIMAGELIST mensaje (Commctrl.h)
description: Recupera el identificador de la lista de imágenes normal o de estado asociada a un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ GetImageList.
ms.assetid: bcf5eac8-cb07-4cf8-ad93-47319fc915a5
keywords:
- TVM_GETIMAGELIST controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b7536f21757d5ad03446654d9eed17444e4e07570c3f4bf032b7d32f0009208
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293285"
---
# <a name="tvm_getimagelist-message"></a>Mensaje \_ GETIMAGELIST de TVM

Recupera el identificador de la lista de imágenes normal o de estado asociada a un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ GetImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de lista de imágenes que se recuperará. Este parámetro puede ser uno de los siguientes valores:



| Valor                                                                                                                                                      | Significado                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <dt>**TVSIL \_ NORMAL**</dt> </dl> | Indica la lista de imágenes normal, que contiene imágenes seleccionadas, no seleccionadas y superpuestas para los elementos de un control de vista de árbol.<br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <dt>**TVSIL \_ STATE**</dt> </dl>    | Indica la lista de imágenes de estado. Puede usar imágenes de estado para indicar los estados de los elementos definidos por la aplicación. Se muestra una imagen de estado a la izquierda de la imagen seleccionada o no seleccionada de un elemento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un identificador HIMAGELIST a la lista de imágenes especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ SETIMAGELIST**](tvm-setimagelist.md)
</dt> </dl>

 

 





