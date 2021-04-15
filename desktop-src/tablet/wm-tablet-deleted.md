---
description: El mensaje de la \_ tableta \_ de WM eliminada se envía cuando se quita un dispositivo de tableta gráfica de Windows.
ms.assetid: af5be7f0-a213-49a1-800e-c922281522c8
title: Mensaje de WM_TABLET_DELETED (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8ade03d199f8ee7a258b9db2aeea039fd725e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696330"
---
# <a name="wm_tablet_deleted-message"></a>\_Mensaje eliminado de Tablet PC de WM \_

El mensaje de la **tableta de WM \_ \_ eliminada** se envía cuando se quita un dispositivo de tableta gráfica de Windows.


```C++
#define WM_TABLET_DEFBASE   0x02C0
#define WM_TABLET_DELETED   (WM_TABLET_DEFBASE + 9)     
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del dispositivo de tableta gráfica que se va a quitar.

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



 

 
