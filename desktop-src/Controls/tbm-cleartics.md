---
title: Mensaje de TBM_CLEARTICS (commctrl. h)
description: Quita las marcas de graduación actuales de una barra de aumento. Este mensaje no quita la primera y última marca de graduación, creadas automáticamente por la barra de aumento.
ms.assetid: 2830497c-2cf0-4068-810c-c05d4e0abb8b
keywords:
- TBM_CLEARTICS controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489814"
---
# <a name="tbm_cleartics-message"></a>TBM \_ CLEARTICS

Quita las marcas de graduación actuales de una barra de aumento. Este mensaje no quita la primera y última marca de graduación, creadas automáticamente por la barra de aumento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Volver a dibujar el marcador. Si este parámetro es **true**, la barra de aumento se vuelve a dibujar una vez que se han desactivado las marcas de graduación. Si este parámetro es **false**, el mensaje borra las marcas de graduación pero no vuelve a dibujar la barra de aumento.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





