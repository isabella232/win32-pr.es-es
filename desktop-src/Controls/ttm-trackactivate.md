---
title: TTM_TRACKACTIVATE mensaje (Commctrl.h)
description: Activa o desactiva una información sobre herramientas de seguimiento.
ms.assetid: 6cf43377-a772-4749-81c4-a685998092e5
keywords:
- TTM_TRACKACTIVATE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165837"
---
# <a name="ttm_trackactivate-message"></a>Mensaje \_ TRACKACTIVATE de TTM

Activa o desactiva una información sobre herramientas de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica si se está activando o desactivando el seguimiento. Este valor puede ser uno de los siguientes:



| Value                                                                                                                                | Significado                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**VERDAD**</dt> </dl>    | Activar seguimiento.<br/>   |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**FALSO**</dt> </dl> | Desactivación del seguimiento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que identifica la herramienta a la que se aplica este mensaje. Los **miembros hwnd** **y uId** identifican la herramienta y el **miembro cbSize** especifica el tamaño de la estructura. Se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TTM \_ TRACKPOSITION**](ttm-trackposition.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Uso de controles de información sobre herramientas](using-tooltip-contro.md)
</dt> </dl>

 

 





