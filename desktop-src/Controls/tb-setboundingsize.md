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
ms.openlocfilehash: 419595da16148f7382da5053d3187e9cce9e00a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166654"
---
# <a name="tb_setboundingsize-message"></a>Mensaje \_ DE TB SETBOUNDINGSIZE

\[Diseñado para uso interno; no se recomienda para su uso en aplicaciones. Es posible que este mensaje no se pueda usar en versiones futuras de Windows.\]

Establece el tamaño de límite de un control de barra de herramientas de varias columnas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura SIZE**](/previous-versions//dd145106(v=vs.85)) cuyo **miembro cy** contiene el alto delimitador. Se omite el miembro **cx** (el ancho).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="security-considerations"></a>Consideraciones de seguridad

El uso de este mensaje podría poner en peligro la seguridad del programa.

## <a name="remarks"></a>Observaciones

El tamaño de límite controla cómo se organizan los botones en columnas. Si el control de barra de herramientas no tiene el [**estilo TBSTYLE \_ EX \_ MULTICOLUMN,**](toolbar-extended-styles.md) este mensaje no tiene ningún efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

