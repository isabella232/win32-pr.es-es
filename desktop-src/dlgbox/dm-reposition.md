---
title: DM_REPOSITION mensaje (Winuser.h)
description: Vuelve a colocar un cuadro de diálogo de nivel superior para que se ajuste al área de escritorio. Una aplicación puede enviar este mensaje a un cuadro de diálogo después de cambiar su tamaño para asegurarse de que todo el cuadro de diálogo permanece visible.
ms.assetid: 8386d23e-06ea-4ea7-adde-ac97fc97861d
keywords:
- DM_REPOSITION cuadros de diálogo del mensaje
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
ms.openlocfilehash: 52fd3978df92e379f4750b4140c137b915d0d1ae21ac0a5124d3e9d87e62d5c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117815"
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

## <a name="remarks"></a>Comentarios

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

 

 





