---
title: TBM_GETBUDDY mensaje (Commctrl.h)
description: Recupera el identificador en una ventana de control de barra de seguimiento en una ubicación determinada. La ubicación especificada es relativa a la orientación del control (horizontal o vertical).
ms.assetid: 69e4e467-150d-4505-b1c2-2ed9dd83f1a6
keywords:
- TBM_GETBUDDY controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_GETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e03053981ed16b97d68d5b2f0c77db64062d64fd2df7b5a347e4757736d4844
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829619"
---
# <a name="tbm_getbuddy-message"></a>Mensaje \_ GETBUDDY de TBM

Recupera el identificador en una ventana de control de barra de seguimiento en una ubicación determinada. La ubicación especificada es relativa a la orientación del control (horizontal o vertical).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que indica qué identificador de ventana de amón se recuperará, por ubicación relativa. Este valor puede ser uno de los siguientes:



| Valor                                                                                                                                    | Significado                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE*"</dt> </dl>    | Recupera el identificador del compañero a la izquierda de la barra de seguimiento. Si el control trackbar usa el [**estilo \_ VERT de TBS,**](trackbar-control-styles.md) el mensaje recuperará el compañero encima de la barra de seguimiento.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE**</dt> </dl> | Recupera el identificador del compañero a la derecha de la barra de seguimiento. Si el control trackbar usa el [**estilo \_ VERT de TBS,**](trackbar-control-styles.md) el mensaje recuperará el compañero debajo de la barra de seguimiento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la ventana del compañero en la ubicación especificada por *wParam* o **NULL** si no existe ninguna ventana de amigos en esa ubicación.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





