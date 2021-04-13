---
title: Mensaje de WM_UNINITMENUPOPUP (Winuser. h)
description: Se envía cuando se destruye un menú desplegable o un submenú.
ms.assetid: 06129d88-6cf9-4d55-b8eb-6f78994bc87a
keywords:
- WM_UNINITMENUPOPUP menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_UNINITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6cb3484ec9ebcd0f62a8c06eb4c23bf5355f1d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535542"
---
# <a name="wm_uninitmenupopup-message"></a>Mensaje de UNINITMENUPOPUP de WM \_

Se envía cuando se destruye un menú desplegable o un submenú.


```C++
#define WM_UNINITMENUPOPUP              0x0125
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del menú.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden superior identifica el menú que se ha destruido. Actualmente, este parámetro solo puede ser **MF \_ SYSMENU** (el menú ventana).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si una aplicación recibe un mensaje de [**\_ INITMENUPOPUP de WM**](wm-initmenupopup.md) , recibirá un mensaje de **\_ UNINITMENUPOPUP de WM** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

**Vista**
</dt> <dt>

[Menús](menus.md)
</dt> </dl>

 

