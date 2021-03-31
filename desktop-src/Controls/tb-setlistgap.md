---
title: Mensaje de TB_SETLISTGAP (commctrl. h)
description: Establece la distancia entre los botones de la barra de herramientas en una barra de herramientas concreta.
ms.assetid: ca8ba6e4-cf70-41ca-ac61-cd13671d4010
keywords:
- TB_SETLISTGAP controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103904984"
---
# <a name="tb_setlistgap-message"></a>\_Mensaje SETLISTGAP TB

Establece la distancia entre los botones de la barra de herramientas en una barra de herramientas concreta.

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

El intervalo entre los botones solo se aplica a la ventana de control de la barra de herramientas que recibe este mensaje. La recepción de este mensaje desencadena un reenvío de la barra de herramientas, si la barra de herramientas está visible actualmente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





