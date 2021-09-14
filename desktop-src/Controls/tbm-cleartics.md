---
title: TBM_CLEARTICS mensaje (Commctrl.h)
description: Quita las marcas de graduación actuales de una barra de seguimiento. Este mensaje no quita la primera y la última marca de graduación, que la barra de seguimiento crea automáticamente.
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
ms.openlocfilehash: 7a1ecb4f9f931c976b2542a1f263fc069f1eca10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166537"
---
# <a name="tbm_cleartics-message"></a>Mensaje \_ CLEARTICS de TBM

Quita las marcas de graduación actuales de una barra de seguimiento. Este mensaje no quita la primera y la última marca de graduación, que la barra de seguimiento crea automáticamente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Vuelva a dibujar la marca. Si este parámetro es **TRUE**, la barra de seguimiento se vuelve a dibujar después de borrar las marcas de graduación. Si este parámetro es **FALSE,** el mensaje borra las marcas de graduación, pero no vuelve a dibujar la barra de seguimiento.

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
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





