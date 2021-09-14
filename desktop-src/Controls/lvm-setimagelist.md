---
title: LVM_SETIMAGELIST mensaje (Commctrl.h)
description: Asigna una lista de imágenes a un control list-view. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView SetImageList.
ms.assetid: 5241065b-85e4-412e-9868-fd5b15ff7c17
keywords:
- LVM_SETIMAGELIST controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 779d31fd781a72dbdfbc4738e091482ca4a08528
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362718"
---
# <a name="lvm_setimagelist-message"></a>Mensaje \_ SETIMAGELIST de LVM

Asigna una lista de imágenes a un control list-view. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView SetImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de lista de imágenes. Este parámetro puede ser uno de los siguientes valores:



| Value                                                                                                                                                                     | Significado                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <dt>**LVSIL \_ NORMAL**</dt> </dl>                | Lista de imágenes con iconos grandes.<br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <dt>**LVSIL \_ SMALL**</dt> </dl>                   | Lista de imágenes con iconos pequeños.<br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <dt>**LVSIL \_ STATE**</dt> </dl>                   | Lista de imágenes con imágenes de estado.<br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <dt>**LVSIL \_ GROUPHEADER**</dt> </dl> | Lista de imágenes para el encabezado de grupo.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la lista de imágenes que se asignará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la lista de imágenes previamente asociada al control si se realiza correctamente o **NULL** en caso contrario.

## <a name="remarks"></a>Observaciones

La lista de imágenes actual se destruirá cuando se destruya el control list-view a menos que se establezca el estilo [**\_ LVS SHAREIMAGELISTS.**](list-view-window-styles.md) Si usa este mensaje para reemplazar una lista de imágenes por otra, la aplicación debe destruir explícitamente todas las listas de imágenes distintas de la actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





