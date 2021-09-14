---
title: LVM_GETGROUPRECT mensaje (Commctrl.h)
description: Obtiene el rectángulo de un grupo especificado. Envíe este mensaje explícitamente o mediante la \_ macro ListView GetGroupRect.
ms.assetid: 9441a6c5-11d8-4f52-80dd-1b60befd9b9d
keywords:
- LVM_GETGROUPRECT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974092"
---
# <a name="lvm_getgrouprect-message"></a>Mensaje \_ GETGROUPRECT de LVM

Obtiene el rectángulo de un grupo especificado. Envíe este mensaje explícitamente o mediante la macro [**\_ ListView GetGroupRect.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Especifica el grupo por **iGroupId** (vea [**ESTRUCTURA LVGROUP).**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) para recibir información sobre el grupo especificado por *wParam*. El receptor del mensaje es responsable de establecer los miembros de la estructura con información para el grupo especificado por *wParam*.

El proceso de llamada es responsable de asignar memoria para la estructura . Establezca el **miembro** superior del [**RECT**](/previous-versions//dd162897(v=vs.85)) en una de las marcas siguientes para especificar las coordenadas del rectángulo que se va a obtener.



| Value                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVGGR_GROUP"></span><span id="lvggr_group"></span><dl> <dt>**LVGGR \_ GROUP**</dt> </dl>                | Coordenadas de todo el grupo expandido.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="LVGGR_HEADER"></span><span id="lvggr_header"></span><dl> <dt>**ENCABEZADO \_ LVGGR**</dt> </dl>             | Coordenadas del encabezado solo (grupo contraído).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="LVGGR_LABEL"></span><span id="lvggr_label"></span><dl> <dt>**LVGGR \_ LABEL**</dt> </dl>                | Solo coordenadas de la etiqueta.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="LVGGR_SUBSETLINK"></span><span id="lvggr_subsetlink"></span><dl> <dt>**LVGGR \_ SUBSETLINK**</dt> </dl> | Coordenadas del vínculo de subconjunto solo (subconjunto de marcado). Un control de vista de lista puede limitar el número de elementos visibles que se muestran en cada grupo. Se presenta un vínculo al usuario para permitir que el usuario expanda el grupo. Esta marca devolverá el rectángulo delimitador del vínculo de subconjunto si el grupo es un subconjunto (estado de grupo de LVGS SUBSETED, vea estructura \_ [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), estado de **miembro**). Esta marca se proporciona para que las aplicaciones de accesibilidad puedan encontrar el vínculo.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

