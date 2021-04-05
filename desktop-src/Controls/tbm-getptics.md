---
title: Mensaje de TBM_GETPTICS (commctrl. h)
description: Recupera la dirección de una matriz que contiene las posiciones de las marcas de paso de una barra de aumento.
ms.assetid: d15a4b4d-2ced-40a4-9351-ed7ecc5a5751
keywords:
- TBM_GETPTICS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETPTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5d81e67156c0118310017413b8e73714246b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996425"
---
# <a name="tbm_getptics-message"></a>TBM \_ GETPTICS

Recupera la dirección de una matriz que contiene las posiciones de las marcas de paso de una barra de aumento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la dirección de una matriz de valores **DWORD** . Los elementos de la matriz especifican las posiciones lógicas de las marcas de graduación de la barra de aumento, sin incluir la primera y la última marca de graduación creada por la barra de aumento. Las posiciones lógicas pueden ser cualquiera de los valores enteros del intervalo de la barra de desplazamiento mínimo y máximo de posiciones de control deslizante.

## <a name="remarks"></a>Observaciones

El número de elementos de la matriz es dos veces menor que el número de pasos devuelto por el mensaje [**\_ GETNUMTICS de TBM**](tbm-getnumtics.md) . Tenga en cuenta que los valores de la matriz pueden incluir posiciones duplicadas y que no estén en orden secuencial. El puntero devuelto es válido hasta que se cambian las marcas de graduación de la barra de resultados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





