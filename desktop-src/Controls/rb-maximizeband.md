---
title: Mensaje de RB_MAXIMIZEBAND (commctrl. h)
description: Cambia el tamaño de una banda de un control rebar a su tamaño ideal o mayor.
ms.assetid: 79fff6d0-01f2-4308-b916-38dc06dad894
keywords:
- RB_MAXIMIZEBAND controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_MAXIMIZEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708a8fae7c0dd8e72eea8e5acefe43ab50054592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905420"
---
# <a name="rb_maximizeband-message"></a>Mensaje de MAXIMIZEBAND de RB \_

Cambia el tamaño de una banda de un control rebar a su tamaño ideal o mayor.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la banda que se va a maximizar.

</dd> <dt>

*lParam* 
</dt> <dd>

Indica si se debe usar el ancho ideal de la banda cuando la banda está maximizada. Si este valor es distinto de cero, se usará el ancho ideal. Si este valor es cero, la banda se hará lo más grande posible.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_SETBANDINFO RB**](rb-setbandinfo.md)
</dt> </dl>

 

 





