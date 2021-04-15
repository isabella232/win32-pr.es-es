---
title: Mensaje de EM_GETFILELINE (CommCtrl. h)
description: Copia una línea de texto de un control de edición, independientemente de cómo se muestran las líneas en la pantalla y la coloca en un búfer especificado.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- EM_GETFILELINE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 6b3be3ea4ae883fc808f7ddc8fb60f0d93bcd6ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491812"
---
# <a name="em_getfileline-message-commctrlh"></a>Mensaje de EM_GETFILELINE (CommCtrl. h)

Copia una línea de texto de un control de edición, independientemente de cómo se muestran las líneas en la pantalla y la coloca en un búfer especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la línea que se va a recuperar de un control de edición multilínea. Un valor de cero especifica la línea superior. Este parámetro se omite en un control de edición de una sola línea.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer que recibe una copia de la línea. Antes de enviar el mensaje, establezca la primera palabra de este búfer en el tamaño, en **TCHAR** s, del búfer. Para texto ANSI, es el número de bytes; en el caso de texto Unicode, es el número de caracteres. La línea copiada sobrescribe el tamaño de la primera palabra.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el número **de elementos** que se han copiado. El valor devuelto es cero si el número de línea especificado por el parámetro *wParam* es mayor que el número de líneas en el control de edición.

## <a name="remarks"></a>Observaciones

La línea copiada no contiene un carácter nulo de terminación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 y 1809 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2019 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_FILELINELENGTH em**](em-filelinelength.md)
</dt> <dt>

[**Editar \_ GetFileLine**](/windows/win32/api/commctrl/nf-commctrl-edit_getfileline)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**GETTEXT de WM \_**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

