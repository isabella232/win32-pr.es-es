---
title: TB_SETEXTENDEDSTYLE mensaje (Commctrl.h)
description: Establece los estilos extendidos para un control de barra de herramientas.
ms.assetid: aec64bc7-74b4-4efc-9864-2c8a9fbd35c2
keywords:
- TB_SETEXTENDEDSTYLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 600e5904637215eeb052c85ec0203c9b86c75ed6b179be643dc9a213156b3afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318885"
---
# <a name="tb_setextendedstyle-message"></a>Mensaje \_ TB SETEXTENDEDSTYLE

Establece los estilos extendidos para un control de barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor que especifica los nuevos estilos extendidos. Este parámetro puede ser una combinación de [estilos extendidos.](toolbar-extended-styles.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **DWORD que** representa los estilos extendidos anteriores. Este valor puede ser una combinación de estilos [extendidos.](toolbar-extended-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TB \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md)
</dt> </dl>

 

 





