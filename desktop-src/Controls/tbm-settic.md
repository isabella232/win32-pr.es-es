---
title: Mensaje de TBM_SETTIC (commctrl. h)
description: Establece una marca de graduación en una barra de aumento en la posición lógica especificada.
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- TBM_SETTIC controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a42839157125c8def28a19dd9c2ccce21d3b96c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150064"
---
# <a name="tbm_settic-message"></a>TBM \_ SETTIC

Establece una marca de graduación en una barra de aumento en la posición lógica especificada.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Posición de la marca de graduación. Este parámetro puede ser cualquiera de los valores enteros en el intervalo de la barra de desplazamiento mínimo y máximo de posiciones de control deslizante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si la marca de graduación está establecida o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Una barra de aumento crea sus propias marcas de graduación primero y último. No utilice este mensaje para establecer la primera y la última marca de graduación.

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

[**TBM \_ GETPTICS**](tbm-getptics.md)
</dt> <dt>

[**TBM \_ GETTIC**](tbm-gettic.md)
</dt> </dl>

 

 





