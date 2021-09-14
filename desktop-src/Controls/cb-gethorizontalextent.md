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
ms.openlocfilehash: 8a2b1fb7c8fe7549360801516364528c9a2ef1f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062543"
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



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CB \_ SETHORIZONTALEXTENT**](cb-sethorizontalextent.md)
</dt> </dl>

 

 





