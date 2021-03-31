---
title: Mensaje de PGM_SETCHILD (commctrl. h)
description: Establece la ventana contenida para el control de paginación.
ms.assetid: 717e6720-aa42-4ecd-9520-4618a04dc28d
keywords:
- PGM_SETCHILD controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150191"
---
# <a name="pgm_setchild-message"></a>\_Mensaje SETCHILD PGM

Establece la ventana contenida para el control de paginación. Este mensaje no cambiará el elemento primario de la ventana contenida; solo asigna un identificador de ventana al control de paginación para el desplazamiento. En la mayoría de los casos, la ventana contenida será una ventana secundaria. En este caso, la ventana contenida debe ser un elemento secundario del control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ SetChild de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la ventana que se va a incluir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





