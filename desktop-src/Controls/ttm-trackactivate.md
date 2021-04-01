---
title: Mensaje de TTM_TRACKACTIVATE (commctrl. h)
description: Activa o desactiva una información sobre herramientas de seguimiento.
ms.assetid: 6cf43377-a772-4749-81c4-a685998092e5
keywords:
- TTM_TRACKACTIVATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_TRACKACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3d0a6caf110045d694208c63aa81d63c265c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996638"
---
# <a name="ttm_trackactivate-message"></a>TTM \_ TRACKACTIVATE

Activa o desactiva una información sobre herramientas de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica si el seguimiento se está activando o desactivando. Este valor puede ser uno de los siguientes:



| Value                                                                                                                                | Significado                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**REALES**</dt> </dl>    | Activar seguimiento.<br/>   |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**ES**</dt> </dl> | Desactivar seguimiento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que identifica la herramienta a la que se aplica este mensaje. Los miembros **hWnd** y **uId** identifican la herramienta y el miembro **cbSize** especifica el tamaño de la estructura. Se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TTM \_ TRACKPOSITION**](ttm-trackposition.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Usar controles ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 





