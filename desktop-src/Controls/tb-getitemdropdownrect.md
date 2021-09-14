---
title: TB_GETITEMDROPDOWNRECT mensaje (Commctrl.h)
description: Obtiene el rectángulo delimitador de la ventana desplegable para un elemento de la barra de herramientas con el estilo BTNS \_ DROPDOWN.
ms.assetid: 4b59c96b-8d75-44c1-b771-c1d62502a2c2
keywords:
- TB_GETITEMDROPDOWNRECT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166798"
---
# <a name="tb_getitemdropdownrect-message"></a>Mensaje \_ DE TB GETITEMDROPDOWNRECT

Obtiene el rectángulo delimitador de la ventana desplegable para un elemento de la barra de herramientas con el estilo [**BTNS \_ DROPDOWN**](toolbar-control-and-button-styles.md).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Índice de base cero del elemento de control de la barra de herramientas para el que se va a recuperar el rectángulo delimitador.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>Puntero a una <a href="/previous-versions//dd162897(v=vs.85)">**estructura RECT**</a> para recibir la información del rectángulo delimitador. El remitente del mensaje es responsable de asignar esta estructura. Las coordenadas devueltas en la **estructura RECT** se expresan como coordenadas de cliente.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve un valor distinto de cero.

## <a name="remarks"></a>Observaciones

El elemento debe tener el [**estilo \_ DESPLEGABLE BTNS.**](toolbar-control-and-button-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

