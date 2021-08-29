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
ms.openlocfilehash: 4b5860a0e7016080c70682d99209b112dc8ab81100ed4d1115db904832f1b92e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825805"
---
# <a name="ttm_trackactivate-message"></a>Mensaje TRACKACTIVATE de TTM \_

Activa o desactiva una información sobre herramientas de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica si se está activando o desactivando el seguimiento. Este valor puede ser uno de los siguientes:



| Value                                                                                                                                | Significado                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**Verdad**</dt> </dl>    | Activar seguimiento.<br/>   |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**Falso**</dt> </dl> | Desactivación del seguimiento.<br/> |



 

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
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TTM \_ TRACKPOSITION**](ttm-trackposition.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Usar controles de información sobre herramientas](using-tooltip-contro.md)
</dt> </dl>

 

 





