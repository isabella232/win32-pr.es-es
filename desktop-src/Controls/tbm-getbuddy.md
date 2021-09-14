---
title: TBM_GETBUDDY mensaje (Commctrl.h)
description: Recupera el identificador en una ventana de compañeros de control de la barra de seguimiento en una ubicación determinada. La ubicación especificada es relativa a la orientación del control (horizontal o vertical).
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
ms.openlocfilehash: b4c076f001a1dff62541c3aa32bc12744b30c012
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166530"
---
# <a name="tbm_getbuddy-message"></a>Mensaje \_ GETBUDDY de TBM

Recupera el identificador en una ventana de compañeros de control de la barra de seguimiento en una ubicación determinada. La ubicación especificada es relativa a la orientación del control (horizontal o vertical).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que indica qué identificador de ventana de compañeros se recuperará, por ubicación relativa. Este valor puede ser uno de los siguientes:



| Value                                                                                                                                    | Significado                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE**</dt> </dl>    | Recupera el identificador del compañero a la izquierda de la barra de seguimiento. Si el control trackbar usa el estilo [**\_ VERT de TBS,**](trackbar-control-styles.md) el mensaje recuperará el compañero encima de la barra de seguimiento.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE**</dt> </dl> | Recupera el identificador del compañero a la derecha de la barra de seguimiento. Si el control trackbar usa el estilo [**\_ VERT de TBS,**](trackbar-control-styles.md) el mensaje recuperará el compañero debajo de la barra de seguimiento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la ventana del compañero en la ubicación especificada por *wParam* o **NULL** si no existe ninguna ventana de compañeros en esa ubicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





