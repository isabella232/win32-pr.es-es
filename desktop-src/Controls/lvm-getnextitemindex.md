---
title: Mensaje de LVM_GETNEXTITEMINDEX (commctrl. h)
description: Recupera el índice de un elemento en un control de vista de lista especificado que coincide con las propiedades y la relación especificadas con otro elemento. Envíe este mensaje explícitamente o mediante la \_ macro GetNextItemIndex de ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getnextitemindex.htm
keywords:
- LVM_GETNEXTITEMINDEX controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150892"
---
# <a name="lvm_getnextitemindex-message"></a>\_Mensaje GETNEXTITEMINDEX LVM

Recupera el índice de un elemento en un control de vista de lista especificado que coincide con las propiedades y la relación especificadas con otro elemento. Envíe este mensaje explícitamente o mediante la [**macro \_ GetNextItemIndex de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnextitemindex) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ in, out\]
</dt> <dd>

Puntero a la estructura [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) del elemento en el que se va a comenzar la búsqueda, o-1 para buscar el primer elemento que coincida con las marcas especificadas. El proceso de llamada es responsable de asignar esta estructura y establecer sus miembros.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica la relación con el elemento incluido en el parámetro *wParam*. Puede ser una combinación de los siguientes valores:



| Value                                                                                                                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>Busca por índice.</dt> </dl>                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_ALL"></span><span id="_______________lvni_all"></span><dl> <dt> **LVNI \_ todo**</dt><dt></dt> </dl>                               | Busca un elemento subsiguiente por índice, el valor predeterminado.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt></dt><dt>Busca por relación física con el índice del elemento en el que va a comenzar la búsqueda.</dt> </dl>                                         |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_ABOVE"></span><span id="_______________lvni_above"></span><dl> <dt> **LVNI \_ anterior**</dt><dt></dt> </dl>                         | Busca un elemento que está por encima del elemento especificado.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_BELOW"></span><span id="_______________lvni_below"></span><dl> <dt> **LVNI \_ a continuación**</dt><dt></dt> </dl>                         | Busca un elemento que está por debajo del elemento especificado.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_TOLEFT"></span><span id="_______________lvni_toleft"></span><dl> <dt> **LVNI \_ TOLEFT**</dt><dt></dt> </dl>                      | Busca un elemento a la izquierda del elemento especificado.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="_______________LVNI_PREVIOUS"></span><span id="_______________lvni_previous"></span><dl> <dt> **LVNI \_ anterior**</dt><dt></dt> </dl>                | **Windows Vista y versiones posteriores:** Busca un elemento que esté ordenado antes del elemento especificado en *wParam*. La marca de LVNI \_ anterior no es direccional (LVNI \_ anterior encontrará el elemento colocado arriba, mientras \_ que LVNI anterior buscará el elemento que se ha ordenado antes). La \_ marca de LVNI anterior básicamente invierte la lógica de la búsqueda realizada por los \_ mensajes GETNEXTITEM o LVM GETNEXTITEMINDEX de LVM \_ .<br/> |
| <span id="_______________LVNI_TORIGHT"></span><span id="_______________lvni_toright"></span><dl> <dt> **LVNI \_ TORIGHT**</dt><dt></dt> </dl>                   | Busca un elemento a la derecha del elemento especificado.<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="_______________LVNI_DIRECTIONMASK"></span><span id="_______________lvni_directionmask"></span><dl> <dt> **LVNI \_ DIRECTIONMASK**</dt><dt></dt> </dl> | **Windows Vista y versiones posteriores:** Una máscara de indicador direccional con valor de la siguiente forma: LVNI \_ sobre \| LVNI por debajo de \_ \| LVNI \_ TOLEFT \| LVNI \_ TORIGHT.<br/>                                                                                                                                                                                                                                                               |
| <dl> <dt></dt><dt>El estado del elemento que se va a buscar se puede especificar con uno o una combinación de los siguientes valores:</dt> </dl>                                |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_CUT"></span><span id="_______________lvni_cut"></span><dl> <dt> **LVNI \_ cortar**</dt><dt></dt> </dl>                               | El elemento tiene establecido el indicador de estado de [**\_ corte de LVIS**](list-view-item-states.md) .<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_DROPHILITED"></span><span id="_______________lvni_drophilited"></span><dl> <dt> **LVNI \_ DROPHILITED**</dt><dt></dt> </dl>       | El elemento tiene establecida la marca de estado [**LVIS \_ DROPHILITED**](list-view-item-states.md)<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="_______________LVNI_FOCUSED"></span><span id="_______________lvni_focused"></span><dl> <dt> **LVNI \_ centrado**</dt><dt></dt> </dl>                   | El elemento tiene establecida la marca de estado de [**LVIS \_ Focused**](list-view-item-states.md) .<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="_______________LVNI_SELECTED"></span><span id="_______________lvni_selected"></span><dl> <dt> **LVNI \_ seleccionado**</dt><dt></dt> </dl>                | El elemento tiene el indicador de estado [**\_ seleccionado LVIS**](list-view-item-states.md) establecido.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="_______________LVNI_STATEMASK"></span><span id="_______________lvni_statemask"></span><dl> <dt> **LVNI \_ STATEMASK**</dt><dt></dt> </dl>             | **Windows Vista y versiones posteriores:** Una marca de estado se enmascara con un valor como sigue: LVNI \_ Focused \| LVNI \_ selected \| LVNI \_ Cut \| LVNI \_ DROPHILITED.<br/>                                                                                                                                                                                                                                                               |
| <dl> <dt></dt><dt>Busca por apariencia de elementos o por grupo.</dt> </dl>                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_VISIBLEORDER"></span><span id="_______________lvni_visibleorder"></span><dl> <dt> **LVNI \_ VISIBLEORDER**</dt><dt></dt> </dl>    | **Windows Vista y versiones posteriores:** Busque el orden visible.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_VISIBLEONLY"></span><span id="_______________lvni_visibleonly"></span><dl> <dt> **LVNI \_ VISIBLEONLY**</dt><dt></dt> </dl>       | **Windows Vista y versiones posteriores:** Busque en los elementos visibles.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_SAMEGROUPONLY"></span><span id="_______________lvni_samegrouponly"></span><dl> <dt> **LVNI \_ SAMEGROUPONLY**</dt><dt></dt> </dl> | **Windows Vista y versiones posteriores:** Buscar en el grupo actual.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt></dt><dt>Si un elemento no tiene todas las marcas de estado especificadas establecidas, la búsqueda continúa con el elemento siguiente.</dt> </dl>                          |                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Tenga en cuenta que las siguientes marcas, solo para su uso con Windows Vista, se excluyen mutuamente de cualquier otra marca en uso: LVNI \_ anterior, LVNI \_ VISIBLEONLY, LVNI \_ SAMEGROUPONLY, LVNI \_ VISIBLEORDER, LVNI \_ DIRECTIONMASK y LVNI \_ STATEMASK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETNEXTITEM LVM**](lvm-getnextitem.md)
</dt> </dl>

 

 





