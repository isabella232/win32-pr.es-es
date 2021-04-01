---
title: Mensaje de LVM_GETIMAGELIST (commctrl. h)
description: Recupera el identificador de una lista de imágenes que se usa para dibujar los elementos de la vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetImageList de ListView.
ms.assetid: dd48d8b5-6dbd-48ab-95c3-0fcf1e8c24f0
keywords:
- LVM_GETIMAGELIST controles de mensajes de Windows
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
ms.openlocfilehash: 0abc68c5e5dd9a18c3ec203ad7fe3db97a542845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150543"
---
# <a name="lvm_getimagelist-message"></a>\_Mensaje GETIMAGELIST LVM

Recupera el identificador de una lista de imágenes que se usa para dibujar los elementos de la vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetImageList de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Lista de imágenes que se va a recuperar. Este parámetro puede ser uno de los siguientes valores:



| Value                                                                                                                                                                     | Significado                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <dt>**LVSIL \_ normal**</dt> </dl>                | Lista de imágenes con iconos grandes.<br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <dt>**LVSIL \_ pequeño**</dt> </dl>                   | Lista de imágenes con iconos pequeños.<br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <dt>**Estado de LVSIL \_**</dt> </dl>                   | Lista de imágenes con imágenes de estado.<br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <dt>**LVSIL \_ encabezadodelgrupo**</dt> </dl> | Lista de imágenes para el encabezado de grupo.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de la lista de imágenes especificada si se realiza correctamente, o **null** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





