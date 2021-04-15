---
title: Mensaje de TBM_GETTIC (commctrl. h)
description: Recupera la posición lógica de una marca de graduación en una barra de aumento. La posición lógica puede ser cualquiera de los valores enteros en el intervalo de la barra de desplazamiento mínimo y máximo de posiciones de control deslizante.
ms.assetid: 9d70c860-de97-4579-bb10-e9e9db7f1784
keywords:
- TBM_GETTIC controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d534d5100e20cc544c31fca2fc9e49cda3bd976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490690"
---
# <a name="tbm_gettic-message"></a>TBM \_ GETTIC

Recupera la posición lógica de una marca de graduación en una barra de aumento. La posición lógica puede ser cualquiera de los valores enteros en el intervalo de la barra de desplazamiento mínimo y máximo de posiciones de control deslizante.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero que identifica una marca de graduación. Los índices válidos están en el intervalo de cero a dos menos que el número de pasos que devuelve el mensaje [**\_ GETNUMTICS de TBM**](tbm-getnumtics.md) .

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la posición lógica de la marca de graduación especificada, o-1 si *wParam* no especifica un índice válido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





