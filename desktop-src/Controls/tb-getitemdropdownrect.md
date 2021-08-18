---
title: TB_GETITEMDROPDOWNRECT mensaje (Commctrl.h)
description: Obtiene el rectángulo delimitador de la ventana desplegable de un elemento de la barra de herramientas con el estilo BTNS \_ DROPDOWN.
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
ms.openlocfilehash: ecd2dfc8a48ff735bfb8bcc99bc0baf36555eee9d995c3f453a95ea2910948a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918705"
---
# <a name="tb_getitemdropdownrect-message"></a>Mensaje \_ GETITEMDROPDOWNRECT de TB

Obtiene el rectángulo delimitador de la ventana desplegable de un elemento de la barra de herramientas con el estilo [**\_ BTNS DROPDOWN**](toolbar-control-and-button-styles.md).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Índice de base cero del elemento de control de barra de herramientas para el que se va a recuperar el rectángulo delimitador.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>Puntero a una <a href="/previous-versions//dd162897(v=vs.85)">**estructura RECT**</a> para recibir la información del rectángulo delimitador. El remitente del mensaje es responsable de asignar esta estructura. Las coordenadas devueltas en la **estructura RECT** se expresan como coordenadas de cliente.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve un valor distinto de cero.

## <a name="remarks"></a>Comentarios

El elemento debe tener el [**estilo \_ DESPLEGABLE BTNS.**](toolbar-control-and-button-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

