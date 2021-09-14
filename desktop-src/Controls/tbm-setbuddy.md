---
title: TBM_SETBUDDY mensaje (Commctrl.h)
description: Asigna una ventana como ventana de compañeros para un control de barra de seguimiento. Las ventanas de barras de seguimiento se muestran automáticamente en una ubicación relativa a la orientación del control (horizontal o vertical).
ms.assetid: ab35911f-bf81-47f3-98aa-0901aa877dea
keywords:
- TBM_SETBUDDY controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166461"
---
# <a name="tbm_setbuddy-message"></a>Mensaje \_ SETBUDDY de TBM

Asigna una ventana como ventana de compañeros para un control de barra de seguimiento. Las ventanas de barras de seguimiento se muestran automáticamente en una ubicación relativa a la orientación del control (horizontal o vertical).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica la ubicación en la que se va a mostrar la ventana del compañero. Este valor puede ser uno de los siguientes:



| Value                                                                                                                                | Significado                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**VERDAD**</dt> </dl>    | El compañero aparecerá a la izquierda de la barra de seguimiento si el control trackbar usa el [**estilo \_ HORZ de TBS.**](trackbar-control-styles.md) Si la barra de seguimiento usa el [**estilo \_ VERT de TBS,**](trackbar-control-styles.md) el compañero aparece encima del control trackbar.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**FALSO**</dt> </dl> | El compañero aparecerá a la derecha de la barra de seguimiento si el control trackbar usa el [**estilo \_ HORZ de TBS.**](trackbar-control-styles.md) Si la barra de seguimiento usa el [**estilo \_ VERT de TBS,**](trackbar-control-styles.md) el compañero aparece debajo del control trackbar.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la ventana que se establecerá como el compañero del control trackbar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la ventana que se asignó previamente al control en esa ubicación.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Los controles de barra de seguimiento admiten hasta dos ventanas de compañeros. Esto puede ser útil cuando debe mostrar texto o imágenes en cada extremo del control.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





