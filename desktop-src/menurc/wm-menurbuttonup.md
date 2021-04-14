---
title: Mensaje de WM_MENURBUTTONUP (Winuser. h)
description: Se envía cuando el usuario suelta el botón secundario del mouse mientras el cursor está en un elemento de menú.
ms.assetid: e061cba0-6aea-4df4-a39a-7e55f0db45c0
keywords:
- WM_MENURBUTTONUP menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_MENURBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7206fc79f6f990611c81ad0e844ae26af3764c6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359868"
---
# <a name="wm_menurbuttonup-message"></a>Mensaje de MENURBUTTONUP de WM \_

Se envía cuando el usuario suelta el botón secundario del mouse mientras el cursor está en un elemento de menú.


```C++
#define WM_MENURBUTTONUP                0x0122
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento de menú en el que se liberó el botón secundario del mouse.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del menú que contiene el elemento.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El mensaje de **\_ MENURBUTTONUP de WM** permite a las aplicaciones proporcionar un menú contextual también conocido como menú contextual para el elemento de menú especificado en este mensaje. Para mostrar un menú contextual de un elemento de menú, llame a la función [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) con el **\_ RECURSE de TPM**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre menús](menus.md)
</dt> </dl>

 

 





