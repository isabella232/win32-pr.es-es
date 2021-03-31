---
title: Código de notificación de EN_IMECHANGE (RichEdit. h)
description: Notifica a un elemento primario del control Rich Edit que ha cambiado el estado de la conversión del IME.
ms.assetid: 2893e4ef-5904-4a57-95c5-3f6cfbb60d90
keywords:
- EN_IMECHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_IMECHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa0e0c8fe4e7d6d8de876a5d1a1fb7a10754096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079405"
---
# <a name="en_imechange-notification-code"></a>\_Código de notificación en IMECHANGE

Notifica a un elemento primario del control Rich Edit que ha cambiado el estado de la conversión del IME. Este código de notificación *solo* está disponible para las versiones de idioma asiático del sistema operativo. Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ comando de WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_IMECHANGE

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control Rich Edit. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del control Rich Edit.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este código de notificación devuelve cero.

## <a name="remarks"></a>Observaciones

Para recibir los \_ códigos de notificación en IMECHANGE, especifique [**ENM \_ IMECHANGE**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .

> [!Note]  
> Este código de notificación solo se admite en la versión asiática de Rich Edit 1,0. No se admite en versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Otros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**comando de WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

