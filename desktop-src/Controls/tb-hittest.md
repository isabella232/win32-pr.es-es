---
title: TB_HITTEST mensaje (Commctrl.h)
description: Determina dónde se encuentra un punto en un control de barra de herramientas.
ms.assetid: d08f3805-2042-470e-8f5a-8a6a681d1189
keywords:
- TB_HITTEST controles de Windows mensaje
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
ms.openlocfilehash: 8d89cecf1d1df5c370ab9a00ae1251df9df7ef919f9959b998407a9fb5881178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696165"
---
# <a name="tb_hittest-message"></a>Mensaje \_ HITTEST de TB

Determina dónde se encuentra un punto en un control de barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura POINT**](/previous-versions//dd162805(v=vs.85)) que contiene la coordenada x de la prueba de acceso en el miembro **x** y la coordenada y de la prueba de acceso en el **miembro y.** Las coordenadas son relativas al área de cliente de la barra de herramientas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero. Si el valor devuelto es cero o un valor positivo, es el índice de base cero del elemento no paraledor en el que se encuentra el punto. Si el valor devuelto es negativo, el punto no se encuentra dentro de un botón. El valor absoluto del valor devuelto es el índice de un elemento separador o el elemento no separador más cercano.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

