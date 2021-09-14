---
title: TBM_GETPTICS mensaje (Commctrl.h)
description: Recupera la dirección de una matriz que contiene las posiciones de las marcas de graduación de una barra de seguimiento.
ms.assetid: d15a4b4d-2ced-40a4-9351-ed7ecc5a5751
keywords:
- TBM_GETPTICS controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166502"
---
# <a name="tbm_getptics-message"></a>Mensaje \_ GETPTICS de TBM

Recupera la dirección de una matriz que contiene las posiciones de las marcas de graduación de una barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la dirección de una matriz de **valores DWORD.** Los elementos de la matriz especifican las posiciones lógicas de las marcas de graduación de la barra de seguimiento, sin incluir la primera y la última marca de graduación creadas por la barra de seguimiento. Las posiciones lógicas pueden ser cualquiera de los valores enteros del intervalo de posiciones del control deslizante mínimo al máximo de la barra de seguimiento.

## <a name="remarks"></a>Observaciones

El número de elementos de la matriz es dos menos que el número de pasos devuelto por el [**mensaje \_ GETNUMTICS de TBM.**](tbm-getnumtics.md) Tenga en cuenta que los valores de la matriz pueden incluir posiciones duplicadas y no estar en orden secuencial. El puntero devuelto es válido hasta que cambie las marcas de graduación de la barra de seguimiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





