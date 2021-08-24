---
title: CB_GETHORIZONTALEXTENT mensaje (Winuser.h)
description: Obtiene el ancho, en píxeles, que el cuadro de lista se puede desplazar horizontalmente (el ancho desplazable). Esto solo es aplicable si el cuadro de lista tiene una barra de desplazamiento horizontal.
ms.assetid: 7c9fff88-2750-4c94-b7f6-6bdd81c224e9
keywords:
- CB_GETHORIZONTALEXTENT controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 928561b812dd3a09909d8d89c7dda1dc67b63f9177769d80db2d16ac78cbbf72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089215"
---
# <a name="cb_gethorizontalextent-message"></a>Mensaje \_ GETHORIZONTALEXTENT de CB

Obtiene el ancho, en píxeles, que el cuadro de lista se puede desplazar horizontalmente (el ancho desplazable). Esto solo es aplicable si el cuadro de lista tiene una barra de desplazamiento horizontal.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el ancho desplazable, en píxeles.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CB \_ SETHORIZONTALEXTENT**](cb-sethorizontalextent.md)
</dt> </dl>

 

 





