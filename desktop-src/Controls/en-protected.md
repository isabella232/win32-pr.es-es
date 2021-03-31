---
title: Código de notificación de EN_PROTECTED (RichEdit. h)
description: Notifica a la ventana primaria de un control Rich Edit que el usuario está realizando una acción que cambiaría un intervalo de texto protegido. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: 29c0cb51-675c-44b1-ad45-5f7140ca5675
keywords:
- EN_PROTECTED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_PROTECTED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1475053366a06f46b0c99514ade961f1a2998b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490870"
---
# <a name="en_protected-notification-code"></a>\_Código de notificación en protegido

Notifica a la ventana primaria de un control Rich Edit que el usuario está realizando una acción que cambiaría un intervalo de texto protegido. Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
EN_PROTECTED

    penProtected = (ENPROTECTED *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**protegida**](/windows/desktop/api/Richedit/ns-richedit-enprotected) que contiene información sobre el mensaje que desencadenó el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para permitir la operación.

Devuelve un valor distinto de cero para evitar la operación.

## <a name="remarks"></a>Observaciones

Si se devuelve cero y se cambian los miembros **MSG**, **wParam** e **lParam** de la estructura [**enprotected**](/windows/desktop/api/Richedit/ns-richedit-enprotected) , el control procesa el mensaje revisado en lugar del mensaje original.

Para recibir \_ códigos de notificación protegidos, especifique [**ENM \_ protegido**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**PROTEGIDO**](/windows/desktop/api/Richedit/ns-richedit-enprotected)
</dt> <dt>

[**\_notificaciones de WM**](wm-notify.md)
</dt> </dl>

 

 





