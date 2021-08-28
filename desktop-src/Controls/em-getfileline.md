---
title: EM_GETFILELINE mensaje (CommCtrl.h)
description: Copia una línea de texto de un control de edición, independientemente de cómo se muestren las líneas en la pantalla y la coloca en un búfer especificado.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- EM_GETFILELINE controles de Windows mensaje
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
ms.openlocfilehash: 470c437280b279f56c3dcc8b45de93cf3f792afc5053b7e312b2c19c7ffcec8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049225"
---
# <a name="em_getfileline-message-commctrlh"></a>EM_GETFILELINE mensaje (CommCtrl.h)

Copia una línea de texto de un control de edición, independientemente de cómo se muestren las líneas en la pantalla y la coloca en un búfer especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la línea que se recuperará de un control de edición multilínea. Un valor de cero especifica la línea superior. Un control de edición de una sola línea omite este parámetro.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer que recibe una copia de la línea. Antes de enviar el mensaje, establezca la primera palabra de este búfer en el tamaño, en **TCHAR,** del búfer. Para el texto ANSI, este es el número de bytes; Para el texto Unicode, este es el número de caracteres. La línea copiada sobrescribe el tamaño de la primera palabra.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el número de **TCHAR** copiados. El valor devuelto es cero si el número de línea especificado por el parámetro *wParam* es mayor que el número de líneas del control de edición.

## <a name="remarks"></a>Comentarios

La línea copiada no contiene un carácter nulo de terminación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio 1809 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2019 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ FILELINELENGTH**](em-filelinelength.md)
</dt> <dt>

[**Editar \_ GetFileLine**](/windows/win32/api/commctrl/nf-commctrl-edit_getfileline)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

