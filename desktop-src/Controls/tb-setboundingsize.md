---
title: TB_SETBOUNDINGSIZE mensaje (Commctrl.h)
description: Establece el tamaño de límite de un control de barra de herramientas de varias columnas.
ms.assetid: f406d9e3-1c40-4317-8cf1-51706f4c6adf
keywords:
- TB_SETBOUNDINGSIZE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETBOUNDINGSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d409769e08e489d922dbdc2361779953555000dca784a6f7b977bbbcd3a5e65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167748"
---
# <a name="tb_setboundingsize-message"></a>Mensaje \_ SETBOUNDINGSIZE de TB

\[Destinado a uso interno; no se recomienda para su uso en aplicaciones. Es posible que este mensaje no se pueda usar en versiones futuras de Windows.\]

Establece el tamaño de límite de un control de barra de herramientas de varias columnas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura SIZE**](/previous-versions//dd145106(v=vs.85)) cuyo **miembro cy** contiene el alto delimitador. Se **omite** el miembro cx (el ancho).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

El uso de este mensaje puede poner en peligro la seguridad del programa.

## <a name="remarks"></a>Comentarios

El tamaño de límite controla cómo se organizan los botones en columnas. Si el control de barra de herramientas no tiene el [**estilo TBSTYLE \_ EX \_ MULTICOLUMN,**](toolbar-extended-styles.md) este mensaje no tiene ningún efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

