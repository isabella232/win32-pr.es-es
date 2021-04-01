---
title: Mensaje de LVM_SETIMAGELIST (commctrl. h)
description: Asigna una lista de imágenes a un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro SetImageList de ListView.
ms.assetid: 5241065b-85e4-412e-9868-fd5b15ff7c17
keywords:
- LVM_SETIMAGELIST controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995934"
---
# <a name="lvm_setimagelist-message"></a>\_Mensaje SETIMAGELIST LVM

Asigna una lista de imágenes a un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetImageList de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de lista de imágenes. Este parámetro puede ser uno de los siguientes valores:



| Value                                                                                                                                                                     | Significado                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <dt>**LVSIL \_ normal**</dt> </dl>                | Lista de imágenes con iconos grandes.<br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <dt>**LVSIL \_ pequeño**</dt> </dl>                   | Lista de imágenes con iconos pequeños.<br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <dt>**Estado de LVSIL \_**</dt> </dl>                   | Lista de imágenes con imágenes de estado.<br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <dt>**LVSIL \_ encabezadodelgrupo**</dt> </dl> | Lista de imágenes para el encabezado de grupo.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la lista de imágenes que se va a asignar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de la lista de imágenes asociada previamente al control si se realiza correctamente, o **null** en caso contrario.

## <a name="remarks"></a>Observaciones

La lista de imágenes actual se destruirá cuando se destruya el control de vista de lista, a menos que se establezca el estilo [**LVS \_ SHAREIMAGELISTS**](list-view-window-styles.md) . Si usa este mensaje para reemplazar una lista de imágenes por otra, la aplicación debe destruir explícitamente todas las listas de imágenes distintas de la actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





