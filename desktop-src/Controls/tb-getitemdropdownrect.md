---
title: Mensaje de TB_GETITEMDROPDOWNRECT (commctrl. h)
description: Obtiene el rectángulo delimitador de la ventana desplegable para un elemento de barra de herramientas con la \_ lista desplegable de estilo BTNS.
ms.assetid: 4b59c96b-8d75-44c1-b771-c1d62502a2c2
keywords:
- TB_GETITEMDROPDOWNRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbcef725b0ade0bfc776200fa5b191618d2ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078995"
---
# <a name="tb_getitemdropdownrect-message"></a>\_Mensaje GETITEMDROPDOWNRECT TB

Obtiene el rectángulo delimitador de la ventana desplegable para un elemento de barra de herramientas con la [**\_ lista desplegable**](toolbar-control-and-button-styles.md)de estilo BTNS.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Índice de base cero del elemento de control de la barra de herramientas para el que se va a recuperar el rectángulo delimitador.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>Puntero a una estructura <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> para recibir la información del rectángulo delimitador. El remitente del mensaje es responsable de la asignación de esta estructura. Las coordenadas devueltas en la estructura **Rect** se expresan como coordenadas de cliente.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve un valor distinto de cero.

## <a name="remarks"></a>Observaciones

El elemento debe tener el estilo de [**\_ lista desplegable BTNS**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

