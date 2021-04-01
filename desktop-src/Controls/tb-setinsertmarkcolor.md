---
title: Mensaje de TB_SETINSERTMARKCOLOR (commctrl. h)
description: Establece el color utilizado para dibujar la marca de inserción de la barra de herramientas.
ms.assetid: 09a04449-9a1f-4f9a-b09f-9f22f930d735
keywords:
- TB_SETINSERTMARKCOLOR controles de mensajes de Windows
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
ms.openlocfilehash: 954654d71a3e3b7bba9af287d3e92fb2362e8711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149886"
---
# <a name="tb_setinsertmarkcolor-message"></a>\_Mensaje SETINSERTMARKCOLOR TB

Establece el color utilizado para dibujar la marca de inserción de la barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor de **COLORREF** que contiene el nuevo color de la marca de inserción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de **COLORREF** que contiene el color anterior de la marca de inserción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TB \_ GETINSERTMARKCOLOR**](tb-getinsertmarkcolor.md)
</dt> </dl>

 

 





