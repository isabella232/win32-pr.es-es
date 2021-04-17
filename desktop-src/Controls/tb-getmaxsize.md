---
title: Mensaje de TB_GETMAXSIZE (commctrl. h)
description: Recupera el tamaño total de todos los botones y separadores visibles en la barra de herramientas.
ms.assetid: 560e6ce2-00ef-46c3-b1d8-fbe0ac79c888
keywords:
- TB_GETMAXSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETMAXSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4829e65d90c04181369dd73b9c54634f1077144
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658287"
---
# <a name="tb_getmaxsize-message"></a>\_Mensaje GETMAXSIZE TB

Recupera el tamaño total de todos los botones y separadores visibles en la barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura de [**tamaño**](/previous-versions//dd145106(v=vs.85)) que recibe el tamaño de los elementos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

