---
description: El mensaje WM TABLET ADDED se publica cuando se agrega un dispositivo de tableta a \_ \_ Windows.
ms.assetid: 74323b34-2364-47eb-b8ac-b97546e43b32
title: WM_TABLET_ADDED mensaje (Tpcshrd.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9c56b475eb63c292d2638d5a34b831862da967868944f823c90b184bdbc076a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934335"
---
# <a name="wm_tablet_added-message"></a>Mensaje \_ de WM TABLET \_ ADDED

El **mensaje WM TABLET \_ \_ ADDED** se publica cuando se agrega un dispositivo de tableta a Windows.


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_ADDED    (WM_TABLET_DEFBASE + 8)      
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de dispositivo de tableta que se va a agregar

</dd> <dt>

*lParam* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Este mensaje se envía a todas las ventanas de nivel superior del sistema, incluidas las ventanas sin control deshabilitadas o invisibles, las ventanas superpuestas y las ventanas emergentes. pero el mensaje no se envía a las ventanas secundarias.

Los índices pasados *en wParam* están relacionados con el índice utilizado por el [**método ITabletManager::GetTablet.**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Header<br/>                   | <dl> <dt>Tpcshrd.h</dt> </dl> |



 

 
