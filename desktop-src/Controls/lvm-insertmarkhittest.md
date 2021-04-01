---
title: Mensaje de LVM_INSERTMARKHITTEST (commctrl. h)
description: Recupera el punto de inserción más cercano a un punto especificado.
ms.assetid: 901bb770-a36d-4d9f-a53b-d497b4df39e5
keywords:
- LVM_INSERTMARKHITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bdb82e924b4a5d74d152917f52c4039e0aca81b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150885"
---
# <a name="lvm_insertmarkhittest-message"></a>\_Mensaje INSERTMARKHITTEST LVM

Recupera el punto de inserción más cercano a un punto especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Puntero a una estructura de **punto** que contiene las coordenadas de la prueba de posicionamiento.</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una estructura <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> que especifica el punto de inserción más cercano a las coordenadas definidas por el parámetro *wParam* .</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario. Se devuelve **false** si el tamaño del miembro **cbSize** de la estructura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) no es igual al tamaño real de la estructura, o cuando no se aplica un punto de inserción en la vista actual.

## <a name="remarks"></a>Observaciones

Un punto de inserción solo puede aparecer si el control de vista de lista está en la vista de iconos, en la vista de iconos pequeños o en la vista de mosaico y no en el modo de vista de grupo.

Si los puntos de inserción no se aplican a la vista, la estructura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) contiene-1 en el miembro **iItem** .

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





