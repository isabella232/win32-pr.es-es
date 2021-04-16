---
description: El mensaje de la tableta de WM \_ \_ agregada se envía cuando se agrega un dispositivo de tableta a Windows.
ms.assetid: 74323b34-2364-47eb-b8ac-b97546e43b32
title: Mensaje de WM_TABLET_ADDED (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a721f83cbab3c520a5502fa2f1262de9a26b25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696331"
---
# <a name="wm_tablet_added-message"></a>\_Mensaje agregado a Tablet PC de WM \_

El mensaje de la **tableta de WM \_ \_ agregada** se envía cuando se agrega un dispositivo de tableta a Windows.


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_ADDED    (WM_TABLET_DEFBASE + 8)      
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del dispositivo de tableta gráfica que se va a agregar

</dd> <dt>

*lParam* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este mensaje se envía a todas las ventanas de nivel superior del sistema, incluidas las ventanas sin propietario deshabilitadas o invisibles, las ventanas superpuestas y las ventanas emergentes. pero el mensaje no se envía a las ventanas secundarias.

Los índices pasados en *wParam* están relacionados con el índice utilizado por el método [**ITabletManager:: GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>Tpcshrd. h</dt> </dl> |



 

 
