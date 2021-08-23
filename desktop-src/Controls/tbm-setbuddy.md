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
ms.openlocfilehash: e4f2586c84740cb2d5e8b1f1aadfb910cd241270d3e18363accf1f166c3c35ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167191"
---
# <a name="tbm_setbuddy-message"></a>Mensaje \_ SETBUDDY de TBM

Asigna una ventana como ventana de compañeros para un control de barra de seguimiento. Las ventanas de barras de seguimiento se muestran automáticamente en una ubicación relativa a la orientación del control (horizontal o vertical).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica la ubicación en la que se va a mostrar la ventana del compañero. Este valor puede ser uno de los siguientes:



| Valor                                                                                                                                | Significado                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**Verdad**</dt> </dl>    | El compañero aparecerá a la izquierda de la barra de seguimiento si el control trackbar usa el [**estilo \_ HORZ de TBS.**](trackbar-control-styles.md) Si la barra de seguimiento usa el [**estilo \_ VERT de TBS,**](trackbar-control-styles.md) el compañero aparece encima del control trackbar.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**Falso**</dt> </dl> | El compañero aparecerá a la derecha de la barra de seguimiento si el control trackbar usa el [**estilo \_ HORZ de TBS.**](trackbar-control-styles.md) Si la barra de seguimiento usa el [**estilo \_ VERT de TBS,**](trackbar-control-styles.md) el compañero aparece debajo del control trackbar.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la ventana que se establecerá como el compañero del control trackbar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la ventana que se asignó previamente al control en esa ubicación.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Los controles de barra de seguimiento admiten hasta dos ventanas de compañeros. Esto puede ser útil cuando debe mostrar texto o imágenes en cada extremo del control.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





