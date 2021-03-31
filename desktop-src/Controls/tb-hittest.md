---
title: Mensaje de TB_HITTEST (commctrl. h)
description: Determina dónde se encuentra un punto en un control de barra de herramientas.
ms.assetid: d08f3805-2042-470e-8f5a-8a6a681d1189
keywords:
- TB_HITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6264bc0191f091d3819081ddd67e428b64c84570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996211"
---
# <a name="tb_hittest-message"></a>TB \_ mensaje HITTEST

Determina dónde se encuentra un punto en un control de barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura de [**punto**](/previous-versions//dd162805(v=vs.85)) que contiene la coordenada x de la prueba de posicionamiento en el miembro **x** y la coordenada y de la prueba de posicionamiento en el miembro **y** . Las coordenadas son relativas al área cliente de la barra de herramientas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero. Si el valor devuelto es cero o un valor positivo, es el índice de base cero del elemento no separador en el que se encuentra el punto. Si el valor devuelto es negativo, el punto no está dentro de un botón. El valor absoluto del valor devuelto es el índice de un elemento separador o el elemento no separador más cercano.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

