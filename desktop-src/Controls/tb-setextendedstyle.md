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
ms.openlocfilehash: b9a540aaeff61bd81b649f0509e064a29282f598
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166621"
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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TB \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md)
</dt> </dl>

 

 





