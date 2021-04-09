---
title: Mensaje de DM_REPOSITION (Winuser. h)
description: Cambia de posición un cuadro de diálogo de nivel superior para que quepa en el área del escritorio. Una aplicación puede enviar este mensaje a un cuadro de diálogo después de cambiar el tamaño para asegurarse de que todo el cuadro de diálogo permanece visible.
ms.assetid: 8386d23e-06ea-4ea7-adde-ac97fc97861d
keywords:
- DM_REPOSITION cuadros de diálogo de mensaje
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079727"
---
# <a name="dm_reposition-message"></a>\_Mensaje de REposición de DM

Cambia de posición un cuadro de diálogo de nivel superior para que quepa en el área del escritorio. Una aplicación puede enviar este mensaje a un cuadro de diálogo después de cambiar el tamaño para asegurarse de que todo el cuadro de diálogo permanece visible.


```C++
#define WM_USER              0x0400
#define DM_REPOSITION       (WM_USER+2)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser cero.

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
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre cuadros de diálogo](dialog-boxes.md)
</dt> </dl>

 

 





