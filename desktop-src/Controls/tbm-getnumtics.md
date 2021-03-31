---
title: Mensaje de TBM_GETNUMTICS (commctrl. h)
description: Recupera el número de marcas de graduación en una barra de aumento.
ms.assetid: 3c3f7ebb-a544-474c-ba14-68eae543ee38
keywords:
- TBM_GETNUMTICS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETNUMTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 712e1a0190334ec279f28a68959f3e3d5d5ffd1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996105"
---
# <a name="tbm_getnumtics-message"></a>TBM \_ GETNUMTICS

Recupera el número de marcas de graduación en una barra de aumento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si no se establece ninguna [marca de graduación](trackbar-control-styles.md) , devuelve 2 para los tics inicial y final. Si se establece [**TBS \_ noticks**](trackbar-control-styles.md) , devuelve cero. De lo contrario, se toma la diferencia entre el intervalo mínimo y el máximo, se divide por la frecuencia de la marca y se agrega 2.

## <a name="remarks"></a>Observaciones

El mensaje **TBM \_ GETNUMTICS** cuenta todas las marcas de graduación, incluidas la primera y la última marca de graduación creadas por la barra de aumento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





