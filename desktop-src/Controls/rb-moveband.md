---
title: Mensaje de RB_MOVEBAND (commctrl. h)
description: Mueve una banda de un índice a otro.
ms.assetid: bb5b45de-957e-46fb-b59a-18b55b69c395
keywords:
- RB_MOVEBAND controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_MOVEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146103c4c3d70fc0514729a00eac152c4847b85c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489233"
---
# <a name="rb_moveband-message"></a>Mensaje de MOVEBAND de RB \_

Mueve una banda de un índice a otro.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la banda que se va a desplace.

</dd> <dt>

*lParam* 
</dt> <dd>

Índice de base cero de la nueva posición de banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="remarks"></a>Observaciones

Probablemente, este mensaje cambiará el índice de otras bandas en el control rebar. Si una banda se mueve del índice 6 al índice 0, se incrementará el índice en todas las bandas entre ellas.

*lParam* nunca debe ser mayor que el número de bandas menos uno. El número de bandas puede obtenerse con el mensaje [**RB \_ GETBANDCOUNT**](rb-getbandcount.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





