---
title: Mensaje de EM_GETLINE (Winuser. h)
description: Copia una línea de texto de un control de edición y la coloca en un búfer especificado. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- EM_GETLINE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e014eaccba65b4ea1fc96e26872954a9cfc06e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996009"
---
# <a name="em_getline-message-winuserh"></a>Mensaje de EM_GETLINE (Winuser. h)

Copia una línea de texto de un control de edición y la coloca en un búfer especificado. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

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

**Controles de edición:** La línea copiada no contiene un carácter nulo de terminación.

**Controles Rich Edit:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. La línea copiada no contiene un carácter nulo de terminación, a menos que no se haya copiado ningún texto. Si no se ha copiado ningún texto, el mensaje coloca un carácter nulo al principio del búfer. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_LINELENGTH em**](em-linelength.md)
</dt> <dt>

[**Editar \_ GetLine**](/windows/desktop/api/Windowsx/nf-windowsx-edit_getline)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**GETTEXT de WM \_**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

