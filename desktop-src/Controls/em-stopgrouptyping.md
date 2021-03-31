---
title: Mensaje EM_STOPGROUPTYPING (RichEdit. h)
description: Detiene un control Rich Edit para recopilar acciones de escritura adicionales en la acción de deshacer actual. El control almacena la siguiente acción de escritura, si existe, en una nueva acción en la cola de deshacer.
ms.assetid: 3059826f-84d1-4b7b-b4a8-da17d5f41013
keywords:
- EM_STOPGROUPTYPING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_STOPGROUPTYPING
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eced7ff12526296552e4adcc38c927ae94ee0502
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802077"
---
# <a name="em_stopgrouptyping-message"></a>\_Mensaje STOPGROUPTYPING em

Detiene un control Rich Edit para recopilar acciones de escritura adicionales en la acción de deshacer actual. El control almacena la siguiente acción de escritura, si existe, en una nueva acción en la cola de deshacer.

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

El valor devuelto es cero. No se puede producir un error en este mensaje.

## <a name="remarks"></a>Observaciones

Un control Rich Edit agrupa acciones de escritura consecutivas, incluidos los caracteres eliminados mediante la tecla **retroceso** , en una sola acción de deshacer hasta que se produce uno de los siguientes eventos:

-   El control recibe un **mensaje \_ STOPGROUPTYPING em** .
-   El control pierde el foco.
-   El usuario mueve la selección actual, ya sea mediante las teclas de dirección o haciendo clic con el mouse.
-   El usuario presiona la tecla **Supr** .
-   El usuario realiza cualquier otra acción, como una operación de pegar que **no** implica la escritura.

Puede enviar el mensaje **\_ STOPGROUPTYPING em** para dividir acciones de escritura consecutivas en grupos de deshacer más pequeños. Por ejemplo, podría enviar **em \_ STOPGROUPTYPING** después de cada carácter o en cada separación de palabras.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**deshacer EM \_**](em-undo.md)
</dt> </dl>

 

 





