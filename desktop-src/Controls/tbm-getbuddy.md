---
title: Mensaje de TBM_GETBUDDY (commctrl. h)
description: Recupera el identificador de una ventana relacionada del control TrackBar en una ubicación determinada. La ubicación especificada es relativa a la orientación del control (horizontal o vertical).
ms.assetid: 69e4e467-150d-4505-b1c2-2ed9dd83f1a6
keywords:
- TBM_GETBUDDY controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997169"
---
# <a name="tbm_getbuddy-message"></a>TBM \_ GETBUDDY

Recupera el identificador de una ventana relacionada del control TrackBar en una ubicación determinada. La ubicación especificada es relativa a la orientación del control (horizontal o vertical).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que indica el identificador de ventana relacionado que se va a recuperar, por ubicación relativa. Este valor puede ser uno de los siguientes:



| Value                                                                                                                                    | Significado                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | Recupera el identificador del Buddy situado a la izquierda de la barra de control. Si el control TrackBar usa el [**estilo \_ vertical de TBS**](trackbar-control-styles.md) , el mensaje recuperará el amigo sobre la barra de control.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Recupera el identificador del relacionado a la derecha de la barra de control. Si el control TrackBar usa el [**estilo \_ vertical de TBS**](trackbar-control-styles.md) , el mensaje recuperará el amigo debajo de la barra de control.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de la ventana relacionada en la ubicación especificada por *wParam*, o **null** si no existe ninguna ventana relacionada en esa ubicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





