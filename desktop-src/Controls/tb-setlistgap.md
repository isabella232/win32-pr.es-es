---
title: TB_SETLISTGAP mensaje (Commctrl.h)
description: Establece la distancia entre los botones de la barra de herramientas de una barra de herramientas específica.
ms.assetid: ca8ba6e4-cf70-41ca-ac61-cd13671d4010
keywords:
- TB_SETLISTGAP controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETLISTGAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 224a709b7beefcfdf49ea7838f905977487aca8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166590"
---
# <a name="tb_setlistgap-message"></a>Mensaje \_ DE TB SETLISTGAP

Establece la distancia entre los botones de la barra de herramientas de una barra de herramientas específica.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Espacio, en píxeles, entre los botones de la barra de herramientas.

</dd> <dt>

*lParam* 
</dt> <dd>

ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La separación entre botones solo se aplica a la ventana de control de la barra de herramientas que recibe este mensaje. La recepción de este mensaje desencadena un repintado de la barra de herramientas, si la barra de herramientas está visible actualmente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





