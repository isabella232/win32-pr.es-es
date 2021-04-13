---
title: Mensaje de WM_ENTERIDLE (Winuser. h)
description: Se envía a la ventana propietaria de un cuadro de diálogo o un menú modal que está entrando en un estado de inactividad. Un cuadro de diálogo o un menú modal entra en un estado de inactividad cuando no hay mensajes en espera en su cola después de haber procesado uno o más mensajes anteriores.
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
ms.openlocfilehash: 4f99b3150a0dbc1a81b78498c8e295fbf2397c22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422502"
---
# <a name="wm_enteridle-message"></a>Mensaje de ENTERIDLE de WM \_

Se envía a la ventana propietaria de un cuadro de diálogo o un menú modal que está entrando en un estado de inactividad. Un cuadro de diálogo o un menú modal entra en un estado de inactividad cuando no hay mensajes en espera en su cola después de haber procesado uno o más mensajes anteriores.


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
| <span id="MSGF_DIALOGBOX"></span><span id="msgf_dialogbox"></span><dl> <dt>**MSGF \_ DIALOGBOX**</dt> <dt>0</dt> </dl> | El sistema está inactivo porque se muestra un cuadro de diálogo.<br/> |
| <span id="MSGF_MENU"></span><span id="msgf_menu"></span><dl> <dt>**MSGF \_ MENÚ**</dt> <dt>2</dt> </dl>                | El sistema está inactivo porque se muestra un menú.<br/>       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Un identificador para el cuadro de diálogo (si *wParam* es **MSGF \_ DIALOGBOX**) o una ventana que contiene el menú mostrado (si *wParam* es el **\_ menú de MSGF**).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Puede suprimir el mensaje de **\_ ENTERIDLE de WM** para un cuadro de diálogo creando el cuadro de diálogo con el estilo **DS \_ NOIDLEMSG** .

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

**Vista**
</dt> <dt>

[Cuadros de diálogo](dialog-boxes.md)
</dt> </dl>

 

