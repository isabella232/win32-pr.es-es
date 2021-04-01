---
title: Mensaje de LVM_GETFOOTERRECT (commctrl. h)
description: Recupera las coordenadas del pie de página de un control de vista de lista. Envíe este mensaje explícitamente o mediante la \_ macro GetFooterRect de ListView.
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- LVM_GETFOOTERRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31df3a1b7b29e5ad9191da9e990e04daec99e948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149900"
---
# <a name="lvm_getfooterrect-message"></a>\_Mensaje GETFOOTERRECT LVM

Recupera las coordenadas del pie de página de un control de vista de lista. Envíe este mensaje explícitamente o mediante la [**macro \_ GetFooterRect de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza. Debe ser 0.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) para recibir las coordenadas. El proceso de llamada es responsable de la asignación de esta estructura. Las coordenadas recibidas se expresan como coordenadas de cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

