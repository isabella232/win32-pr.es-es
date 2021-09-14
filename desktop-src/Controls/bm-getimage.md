---
title: BM_GETIMAGE mensaje (Winuser.h)
description: Recupera un identificador de la imagen (icono o mapa de bits) asociado al botón.
ms.assetid: 766ea1b0-418d-41b8-b31d-0fcc58e03893
keywords:
- BM_GETIMAGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- BM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9319f5310b40ff76a011e1a06b2be1d41be611f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362734"
---
# <a name="bm_getimage-message"></a>Mensaje \_ GETIMAGE de BM

Recupera un identificador de la imagen (icono o mapa de bits) asociado al botón.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de imagen que se asociará al botón. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                      | Significado              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**MAPA DE BITS \_ DE IMAGEN**</dt> </dl> | Mapa de bits.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**ICONO DE \_ IMAGEN**</dt> </dl>       | Un icono.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un identificador de la imagen, si existe; de lo contrario, es **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**BM \_ SETIMAGE**](bm-setimage.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Botones](buttons.md)
</dt> </dl>

 

 





