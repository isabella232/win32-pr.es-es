---
title: STM_GETIMAGE mensaje (Winuser.h)
description: Una aplicación envía un mensaje GETIMAGE STM para recuperar un identificador de la imagen (icono o mapa de \_ bits) asociado a un control estático.
ms.assetid: eb5fe67a-09be-4c13-89c6-0e2f23e8c081
keywords:
- STM_GETIMAGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- STM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77fe0c3d00a2a957530160a5ce5a21b8a1cf84e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167002"
---
# <a name="stm_getimage-message"></a>Mensaje \_ GETIMAGE de STM

Una aplicación envía un mensaje **\_ GETIMAGE STM** para recuperar un identificador de la imagen (icono o mapa de bits) asociado a un control estático.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el tipo de imagen que se recuperará. Este parámetro puede ser uno de los siguientes valores:



| Value                                                                                                                                                                     | Significado                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**IMAGEN DE \_ MAPA DE BITS**</dt> </dl>                | Bits.<br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <dt>**IMAGE \_ CURSOR**</dt> </dl>                | Cursor.<br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <dt>**IMAGE \_ ENHMETAFILE**</dt> </dl> | Metarchivo mejorado.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**ICONO DE \_ IMAGEN**</dt> </dl>                      | Icono.<br/>              |



 

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**STM \_ SETIMAGE**](stm-setimage.md)
</dt> </dl>

 

 





