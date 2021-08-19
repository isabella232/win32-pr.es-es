---
title: TBM_CLEARTICS mensaje (Commctrl.h)
description: Quita las marcas de graduación actuales de una barra de seguimiento. Este mensaje no quita las marcas de graduación primera y última, creadas automáticamente por la barra de seguimiento.
ms.assetid: 2830497c-2cf0-4068-810c-c05d4e0abb8b
keywords:
- TBM_CLEARTICS controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_CLEARTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9390fc45c5b96a7b85d3b1b366e34d24c3b4bf0bc60ec066ead28357bcec1439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046775"
---
# <a name="tbm_cleartics-message"></a>Mensaje \_ CLEARTICS de TBM

Quita las marcas de graduación actuales de una barra de seguimiento. Este mensaje no quita las marcas de graduación primera y última, creadas automáticamente por la barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Volver a dibujar la marca. Si este parámetro es **TRUE,** la barra de seguimiento se vuelve a dibujar después de borrar las marcas de graduación. Si este parámetro es **FALSE,** el mensaje borra las marcas de graduación, pero no vuelve a dibujar la barra de seguimiento.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





