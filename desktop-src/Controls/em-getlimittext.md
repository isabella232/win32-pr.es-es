---
title: Mensaje de EM_GETLIMITTEXT (Winuser. h)
description: Obtiene el límite de texto actual para un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 778967f0-c090-46a2-9f27-194b17bbb1be
keywords:
- EM_GETLIMITTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53da76f43716fd7934011a96d449ffa37c254cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905038"
---
# <a name="em_getlimittext-message"></a>\_Mensaje GETLIMITTEXT em

Obtiene el límite de texto actual para un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el límite del texto.

## <a name="remarks"></a>Observaciones

**Controles de edición, edición enriquecida 2,0 y versiones posteriores:** El límite de texto es la cantidad máxima de texto, en **TCHAR** s, que puede contener el control. Para texto ANSI, es el número de bytes; en el caso de texto Unicode, es el número de caracteres. Dos documentos con el mismo límite de caracteres producirán el mismo límite de texto, aunque uno sea ANSI y el otro sea Unicode.

**Rich Edit 1,0:** El límite de texto es la cantidad máxima de texto, en bytes, que puede contener el control Rich Edit.

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETLIMITTEXT em**](em-setlimittext.md)
</dt> </dl>

 

 





