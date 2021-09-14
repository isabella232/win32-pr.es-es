---
title: EM_STOPGROUPTYPING mensaje (Richedit.h)
description: Impide que un control de edición enriquecido recopile acciones de escritura adicionales en la acción de deshacer actual. El control almacena la siguiente acción de escritura, si la hay, en una nueva acción de la cola de deshacer.
ms.assetid: 3059826f-84d1-4b7b-b4a8-da17d5f41013
keywords:
- EM_STOPGROUPTYPING controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062053"
---
# <a name="em_stopgrouptyping-message"></a>Mensaje EM \_ STOPGROUPTYPING

Impide que un control de edición enriquecido recopile acciones de escritura adicionales en la acción de deshacer actual. El control almacena la siguiente acción de escritura, si la hay, en una nueva acción de la cola de deshacer.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es cero. No se puede producir un error en este mensaje.

## <a name="remarks"></a>Observaciones

Un control de edición enriquecido agrupa las acciones de escritura consecutivas, incluidos los caracteres eliminados mediante la tecla **Retroceso,** en una única acción de deshacer hasta que se produzca uno de los siguientes eventos:

-   El control recibe un **mensaje EM \_ STOPGROUPTYPING.**
-   El control pierde el foco.
-   El usuario mueve la selección actual, ya sea mediante las teclas de dirección o haciendo clic con el mouse.
-   El usuario presiona la **tecla** Eliminar.
-   El usuario realiza cualquier otra acción, como una operación de pegado que **no implica** escribir.

Puede enviar el mensaje **EM \_ STOPGROUPTYPING** para interrumpir las acciones de escritura consecutivas en grupos de deshacer más pequeños. Por ejemplo, podría enviar **EM \_ STOPGROUPTYPING** después de cada carácter o en cada salto de palabra.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> </dl>

 

 





