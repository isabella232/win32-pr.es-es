---
title: Mensaje de PBM_SETBARCOLOR (commctrl. h)
description: Establece el color de la barra de indicador de progreso en el control de barra de progreso.
ms.assetid: 4b512420-04ec-4884-ab13-4c58304b95f6
keywords:
- PBM_SETBARCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_SETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1387e69622e84990a197dc5a374d1c3449393408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534672"
---
# <a name="pbm_setbarcolor-message"></a>Mensaje de SETBARCOLOR de PBM \_

Establece el color de la barra de indicador de progreso en el control de barra de progreso.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor **COLORREF** que especifica el nuevo color de la barra del indicador de progreso. Si se especifica el \_ valor predeterminado de CLR, la barra de progreso usará el color predeterminado de la barra del indicador de progreso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el color de la barra del indicador de progreso anterior, o el \_ valor predeterminado de CLR si el color de la barra indicadora de progreso es el color predeterminado.

## <a name="remarks"></a>Observaciones

Cuando los estilos visuales están habilitados, este mensaje no tiene ningún efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





