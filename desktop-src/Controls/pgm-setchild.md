---
title: PGM_SETCHILD mensaje (Commctrl.h)
description: Establece la ventana independiente para el control de paginación.
ms.assetid: 717e6720-aa42-4ecd-9520-4618a04dc28d
keywords:
- PGM_SETCHILD controles de Windows mensaje
topic_type:
- apiref
api_name:
- PGM_SETCHILD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c934c3c5688ac79b5c5ce67aef68e28ad3627ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167686"
---
# <a name="pgm_setchild-message"></a>Mensaje \_ SETCHILD de PGM

Establece la ventana independiente para el control de paginación. Este mensaje no cambiará el elemento primario de la ventana independiente; solo asigna un identificador de ventana al control de paginación para el desplazamiento. En la mayoría de los casos, la ventana independiente será una ventana secundaria. Si este es el caso, la ventana independiente debe ser un elemento secundario del control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**Pager \_ SetChild.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la ventana que se va a contener.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





