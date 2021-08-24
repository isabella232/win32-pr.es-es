---
title: TB_SETINSERTMARKCOLOR mensaje (Commctrl.h)
description: Establece el color utilizado para dibujar la marca de inserción de la barra de herramientas.
ms.assetid: 09a04449-9a1f-4f9a-b09f-9f22f930d735
keywords:
- TB_SETINSERTMARKCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 466c9bfe27462b11cc0c6cf3a183328ddedb1b422b4d0c07b4496c7a90f83890
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540045"
---
# <a name="tb_setinsertmarkcolor-message"></a>Mensaje \_ TB SETINSERTMARKCOLOR

Establece el color utilizado para dibujar la marca de inserción de la barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

**Valor COLORREF** que contiene el nuevo color de la marca de inserción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor COLORREF** que contiene el color de la marca de inserción anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TB \_ GETINSERTMARKCOLOR**](tb-getinsertmarkcolor.md)
</dt> </dl>

 

 





