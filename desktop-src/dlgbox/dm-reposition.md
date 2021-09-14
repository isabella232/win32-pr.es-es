---
title: DM_REPOSITION mensaje (Winuser.h)
description: Vuelve a colocar un cuadro de diálogo de nivel superior para que se ajuste al área de escritorio. Una aplicación puede enviar este mensaje a un cuadro de diálogo después de cambiar su tamaño para asegurarse de que todo el cuadro de diálogo permanece visible.
ms.assetid: 8386d23e-06ea-4ea7-adde-ac97fc97861d
keywords:
- DM_REPOSITION de diálogo de mensaje
topic_type:
- apiref
api_name:
- DM_REPOSITION
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19425d4d77a62117f3fadfdd98f0629b81bf334c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241371"
---
# <a name="dm_reposition-message"></a>Mensaje \_ DM REPOSITION

Vuelve a colocar un cuadro de diálogo de nivel superior para que se ajuste al área de escritorio. Una aplicación puede enviar este mensaje a un cuadro de diálogo después de cambiar su tamaño para asegurarse de que todo el cuadro de diálogo permanece visible.


```C++
#define WM_USER              0x0400
#define DM_REPOSITION       (WM_USER+2)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa y debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

Este mensaje no tiene ningún efecto si el cuadro de diálogo es una ventana secundaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre cuadros de diálogo](dialog-boxes.md)
</dt> </dl>

 

 





