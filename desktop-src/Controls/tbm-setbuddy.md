---
title: Mensaje de TBM_SETBUDDY (commctrl. h)
description: Asigna una ventana como la ventana relacionada para un control TrackBar. Las ventanas de amigos de la barra de desplazamiento se muestran automáticamente en una ubicación relativa a la orientación del control (horizontal o vertical).
ms.assetid: ab35911f-bf81-47f3-98aa-0901aa877dea
keywords:
- TBM_SETBUDDY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab33e53117933390d7a34ec75a49724003255108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079072"
---
# <a name="tbm_setbuddy-message"></a>TBM \_ SETBUDDY

Asigna una ventana como la ventana relacionada para un control TrackBar. Las ventanas de amigos de la barra de desplazamiento se muestran automáticamente en una ubicación relativa a la orientación del control (horizontal o vertical).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica la ubicación en la que se va a mostrar la ventana relacionada. Este valor puede ser uno de los siguientes:



| Value                                                                                                                                | Significado                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**REALES**</dt> </dl>    | El amigo aparecerá a la izquierda del control TrackBar si el control TrackBar usa el estilo [**TBS \_ horizontal**](trackbar-control-styles.md) . Si la barra de mandos usa el estilo [**\_ vertical de TBS**](trackbar-control-styles.md) , el amigo aparece sobre el control TrackBar.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**ES**</dt> </dl> | El amigo aparecerá a la derecha del control TrackBar si el control TrackBar usa el estilo [**TBS \_ horizontal**](trackbar-control-styles.md) . Si la barra de mandos usa el estilo [**\_ vertical de TBS**](trackbar-control-styles.md) , el amigo aparece debajo del control TrackBar.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la ventana que se establecerá como el Buddy del control TrackBar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de la ventana que se asignó previamente al control en esa ubicación.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Los controles de barra de seguimiento admiten hasta dos ventanas relacionadas. Esto puede ser útil cuando se debe mostrar texto o imágenes en cada extremo del control.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





