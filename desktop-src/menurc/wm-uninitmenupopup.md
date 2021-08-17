---
title: WM_UNINITMENUPOPUP mensaje (Winuser.h)
description: Se envía cuando se destruye un menú desplegable o submenú.
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
ms.openlocfilehash: 7356c0aa4aa62521d2ab998773d07b8aa1a107c92b541c556756a567d31a09a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971794"
---
# <a name="wm_uninitmenupopup-message"></a>Mensaje \_ WM UNINITMENUPOPUP

Se envía cuando se destruye un menú desplegable o submenú.


```C++
#define WM_UNINITMENUPOPUP              0x0125
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del menú

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden superior identifica el menú que se destruyó. Actualmente, este parámetro solo puede ser **MF \_ SYSMENU** (el menú de la ventana).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si una aplicación recibe un [**mensaje \_ WM INITMENUPOPUP,**](wm-initmenupopup.md) recibirá un mensaje **WM \_ UNINITMENUPOPUP.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

**Conceptual**
</dt> <dt>

[Menús](menus.md)
</dt> </dl>

 

