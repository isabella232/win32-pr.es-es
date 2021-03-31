---
title: Mensaje de LVM_GETGROUPRECT (commctrl. h)
description: Obtiene el rectángulo para un grupo especificado. Envíe este mensaje explícitamente o mediante la \_ macro GetGroupRect de ListView.
ms.assetid: 9441a6c5-11d8-4f52-80dd-1b60befd9b9d
keywords:
- LVM_GETGROUPRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2cbdfb1ec6e670e7b5d333694f3a1ca56d287b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995977"
---
# <a name="lvm_getgrouprect-message"></a>\_Mensaje GETGROUPRECT LVM

Obtiene el rectángulo para un grupo especificado. Envíe este mensaje explícitamente o mediante la [**macro \_ GetGroupRect de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Especifica el grupo por **iGroupId** (vea la estructura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) para recibir información sobre el grupo especificado por *wParam*. El receptor del mensaje es responsable de establecer los miembros de la estructura con información para el grupo especificado por *wParam*.

El proceso de llamada es responsable de la asignación de memoria para la estructura. Establezca el miembro **superior** del [**Rect**](/previous-versions//dd162897(v=vs.85)) en una de las marcas siguientes para especificar las coordenadas del rectángulo que se va a obtener.



| Value                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVGGR_GROUP"></span><span id="lvggr_group"></span><dl> <dt>**\_Grupo LVGGR**</dt> </dl>                | Coordenadas de todo el grupo expandido.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="LVGGR_HEADER"></span><span id="lvggr_header"></span><dl> <dt>**\_encabezado LVGGR**</dt> </dl>             | Solo las coordenadas del encabezado (grupo contraído).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="LVGGR_LABEL"></span><span id="lvggr_label"></span><dl> <dt>**\_etiqueta LVGGR**</dt> </dl>                | Solo las coordenadas de la etiqueta.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="LVGGR_SUBSETLINK"></span><span id="lvggr_subsetlink"></span><dl> <dt>**LVGGR \_ SUBSETLINK**</dt> </dl> | Coordenadas solo del vínculo de subconjunto (subconjunto de marcado). Un control de vista de lista puede limitar el número de elementos visibles que se muestran en cada grupo. Se presenta un vínculo al usuario para que el usuario pueda expandir el grupo. Esta marca devolverá el rectángulo delimitador del vínculo de subconjunto si el grupo es un subconjunto (estado de grupo de LVGS \_ subconjunto, consulte la estructura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), **Estado** miembro). Esta marca se proporciona para que las aplicaciones de accesibilidad puedan encontrar el vínculo.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

