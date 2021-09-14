---
title: LVM_GETNEXTITEMINDEX mensaje (Commctrl.h)
description: Recupera el índice de un elemento en un control de vista de lista especificado que coincide con las propiedades especificadas y la relación con otro elemento. Envíe este mensaje explícitamente o mediante la \_ macro ListView GetNextItemIndex.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getnextitemindex.htm
keywords:
- LVM_GETNEXTITEMINDEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETNEXTITEMINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cfc393aee4f275e941a04bb3f23ee4c2c3ac529
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974085"
---
# <a name="lvm_getnextitemindex-message"></a>Mensaje \_ LVM GETNEXTITEMINDEX

Recupera el índice de un elemento en un control de vista de lista especificado que coincide con las propiedades especificadas y la relación con otro elemento. Envíe este mensaje explícitamente o mediante la macro [**\_ ListView GetNextItemIndex.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnextitemindex)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ in, out\]
</dt> <dd>

Puntero a la [**estructura LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) del elemento con el que se iniciará la búsqueda, o -1 para buscar el primer elemento que coincida con las marcas especificadas. El proceso de llamada es responsable de asignar esta estructura y establecer sus miembros.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica la relación con el elemento enumerado en el parámetro *wParam*. Puede ser uno o una combinación de los valores siguientes:



| Value                                                                                                                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>Busca por índice.</dt> </dl>                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_ALL"></span><span id="_______________lvni_all"></span><dl> <dt> **LVNI \_ ALL**</dt><dt></dt> </dl>                               | Busca un elemento posterior por índice, el valor predeterminado.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt></dt><dt>Busca por relación física con el índice del elemento donde se va a iniciar la búsqueda.</dt> </dl>                                         |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_ABOVE"></span><span id="_______________lvni_above"></span><dl> <dt> **LVNI \_ ANTERIOR**</dt><dt></dt> </dl>                         | Busca un elemento que esté por encima del elemento especificado.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_BELOW"></span><span id="_______________lvni_below"></span><dl> <dt> **LVNI \_ A CONTINUACIÓN**</dt><dt></dt> </dl>                         | Busca un elemento que esté debajo del elemento especificado.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_TOLEFT"></span><span id="_______________lvni_toleft"></span><dl> <dt> **LVNI \_ TOLEFT**</dt><dt></dt> </dl>                      | Busca un elemento a la izquierda del elemento especificado.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="_______________LVNI_PREVIOUS"></span><span id="_______________lvni_previous"></span><dl> <dt> **LVNI \_ ANTERIOR**</dt><dt></dt> </dl>                | **Windows Vista y versiones posteriores:** Busca un elemento que se ordena antes que el elemento especificado en *wParam*. La marca LVNI PREVIOUS no es direccional (LVNI ABOVE encontrará el elemento situado anteriormente, mientras que LVNI PREVIOUS encontrará el elemento ordenado \_ \_ \_ antes). La marca LVNI PREVIOUS básicamente invierte la lógica de la búsqueda realizada por los mensajes \_ LVM \_ GETNEXTITEM o LVM \_ GETNEXTITEMINDEX.<br/> |
| <span id="_______________LVNI_TORIGHT"></span><span id="_______________lvni_toright"></span><dl> <dt> **LVNI \_ TORIGHT**</dt><dt></dt> </dl>                   | Busca un elemento a la derecha del elemento especificado.<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="_______________LVNI_DIRECTIONMASK"></span><span id="_______________lvni_directionmask"></span><dl> <dt> **LVNI \_ DIRECTIONMASK**</dt><dt></dt> </dl> | **Windows Vista y versiones posteriores:** Máscara de marca direccional con el valor siguiente: LVNI \_ ABOVE \| LVNI \_ BELOW \| LVNI \_ TOLEFT \| LVNI \_ TORIGHT.<br/>                                                                                                                                                                                                                                                               |
| <dl> <dt></dt>El estado del elemento que se va a buscar se puede <dt>especificar con uno o una combinación de los valores siguientes:</dt> </dl>                                |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_CUT"></span><span id="_______________lvni_cut"></span><dl> <dt> **LVNI \_ CUT**</dt><dt></dt> </dl>                               | El elemento tiene establecida la marca de estado CUT de [**LVIS. \_**](list-view-item-states.md)<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_DROPHILITED"></span><span id="_______________lvni_drophilited"></span><dl> <dt> **LVNI \_ DROPHILITED**</dt><dt></dt> </dl>       | El elemento tiene establecida la marca de estado [**\_ DROPHILITED**](list-view-item-states.md) de LVIS<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="_______________LVNI_FOCUSED"></span><span id="_______________lvni_focused"></span><dl> <dt> **LVNI \_ CENTRADO**</dt><dt></dt> </dl>                   | El elemento tiene establecida la [**marca de estado LVIS \_ FOCUSED.**](list-view-item-states.md)<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="_______________LVNI_SELECTED"></span><span id="_______________lvni_selected"></span><dl> <dt> **LVNI \_ SELECCIONADO**</dt><dt></dt> </dl>                | El elemento tiene establecida la [**marca de estado LVIS \_ SELECTED.**](list-view-item-states.md)<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="_______________LVNI_STATEMASK"></span><span id="_______________lvni_statemask"></span><dl> <dt> **LVNI \_ STATEMASK**</dt><dt></dt> </dl>             | **Windows Vista y versiones posteriores:** Máscara de marca de estado con el valor siguiente: LVNI \_ FOCUSED \| LVNI \_ SELECTED \| LVNI \_ CUT \| LVNI \_ DROPHILITED.<br/>                                                                                                                                                                                                                                                               |
| <dl> <dt></dt><dt>Busca por apariencia de elementos o por grupo.</dt> </dl>                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_VISIBLEORDER"></span><span id="_______________lvni_visibleorder"></span><dl> <dt> **LVNI \_ VISIBLEORDER**</dt><dt></dt> </dl>    | **Windows Vista y versiones posteriores:** Busque el orden visible.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_VISIBLEONLY"></span><span id="_______________lvni_visibleonly"></span><dl> <dt> **LVNI \_ VISIBLEONLY**</dt><dt></dt> </dl>       | **Windows Vista y versiones posteriores:** Buscar en los elementos visibles.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_SAMEGROUPONLY"></span><span id="_______________lvni_samegrouponly"></span><dl> <dt> **LVNI \_ SAMEGROUPONLY**</dt><dt></dt> </dl> | **Windows Vista y versiones posteriores:** Busque en el grupo actual.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt></dt>Si un elemento no tiene todas las marcas de estado <dt>especificadas establecidas, la búsqueda continúa con el siguiente elemento.</dt> </dl>                          |                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Observaciones

Tenga en cuenta que las marcas siguientes, para su uso solo con Windows Vista, son mutuamente excluyentes de cualquier otra marca en uso: LVNI \_ PREVIOUS, LVNI \_ VISIBLEONLY, LVNI \_ SAMEGROUPONLY, LVNI \_ VISIBLEORDER, LVNI \_ DIRECTIONMASK y LVNI \_ STATEMASK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LVM \_ GETNEXTITEM**](lvm-getnextitem.md)
</dt> </dl>

 

 





