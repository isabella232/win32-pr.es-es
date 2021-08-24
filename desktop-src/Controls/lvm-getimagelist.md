---
title: LVM_GETIMAGELIST mensaje (Commctrl.h)
description: Recupera el identificador de una lista de imágenes utilizada para dibujar elementos de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView GetImageList.
ms.assetid: dd48d8b5-6dbd-48ab-95c3-0fcf1e8c24f0
keywords:
- LVM_GETIMAGELIST controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339de36c85b4a5d39476a93cde71cbc6db23d1bc08946d3ce2d1ab1b5a4cb926
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540815"
---
# <a name="lvm_getimagelist-message"></a>Mensaje \_ GETIMAGELIST de LVM

Recupera el identificador de una lista de imágenes utilizada para dibujar elementos de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView GetImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Lista de imágenes que se recuperarán. Este parámetro puede ser uno de los siguientes valores:



| Valor                                                                                                                                                                     | Significado                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <dt>**LVSIL \_ NORMAL**</dt> </dl>                | Lista de imágenes con iconos grandes.<br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <dt>**LVSIL \_ SMALL**</dt> </dl>                   | Lista de imágenes con iconos pequeños.<br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <dt>**LVSIL \_ STATE**</dt> </dl>                   | Lista de imágenes con imágenes de estado.<br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <dt>**LVSIL \_ GROUPHEADER**</dt> </dl> | Lista de imágenes para el encabezado de grupo.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la lista de imágenes especificada si se realiza correctamente o NULL en **caso** contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





