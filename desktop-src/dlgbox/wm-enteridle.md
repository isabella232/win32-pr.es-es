---
title: WM_ENTERIDLE mensaje (Winuser.h)
description: Se envía a la ventana de propietario de un cuadro de diálogo modal o menú que entra en un estado inactivo. Un cuadro de diálogo modal o un menú entra en un estado inactivo cuando no hay ningún mensaje en espera en su cola después de haber procesado uno o varios mensajes anteriores.
ms.assetid: 11b1f942-185f-4de4-90a2-e2934bb1394f
keywords:
- WM_ENTERIDLE cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_ENTERIDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb7d40ae84659d1cfad12357956c4a955ae4f879cddcc13b51069a6a62cd08c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985285"
---
# <a name="wm_enteridle-message"></a>Mensaje \_ ENTERIDLE de WM

Se envía a la ventana de propietario de un cuadro de diálogo modal o menú que entra en un estado inactivo. Un cuadro de diálogo modal o un menú entra en un estado inactivo cuando no hay ningún mensaje en espera en su cola después de haber procesado uno o varios mensajes anteriores.


```C++
#define WM_ENTERIDLE                    0x0121
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                   | Significado                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="MSGF_DIALOGBOX"></span><span id="msgf_dialogbox"></span><dl> <dt>**MSGF \_ CUADRO DE DIÁLOGO**</dt> <dt>0</dt> </dl> | El sistema está inactivo porque se muestra un cuadro de diálogo.<br/> |
| <span id="MSGF_MENU"></span><span id="msgf_menu"></span><dl> <dt>**MSGF \_ MENÚ**</dt> <dt>2</dt> </dl>                | El sistema está inactivo porque se muestra un menú.<br/>       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del cuadro de diálogo (si *wParam* es **MSGF \_ DIALOGBOX)** o una ventana que contiene el menú mostrado (si *wParam* es **MSGF \_ MENU**).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Comentarios

Puede suprimir el mensaje **\_ ENTERIDLE** de WM para un cuadro de diálogo creando el cuadro de diálogo con el estilo **\_ DS NOIDLEMSG.**

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Cuadros de diálogo](dialog-boxes.md)
</dt> </dl>

 

