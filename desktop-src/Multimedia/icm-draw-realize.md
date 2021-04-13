---
title: Mensaje de ICM_DRAW_REALIZE (VFW. h)
description: El mensaje de presentación de ICM de ICM \_ \_ notifica a un controlador de representación que debe observar su paleta de dibujo durante el dibujo. Puede enviar este mensaje explícitamente o mediante la macro ICDrawRealize.
ms.assetid: 501540cd-41e2-4f80-abf8-2ec2179970a9
keywords:
- Mensaje de ICM_DRAW_REALIZE de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd054c16caae55cba25c30098337e54b0ec4b681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422227"
---
# <a name="icm_draw_realize-message"></a>Mensaje de error de \_ Draw de ICM \_

El mensaje de presentación de **ICM de ICM \_ \_** notifica a un controlador de representación que debe observar su paleta de dibujo durante el dibujo. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) .


```C++
ICM_DRAW_REALIZE 
wParam = (DWORD_PTR) (UINT_PTR) (HDC) hdc; 
lParam = (DWORD_PTR) (BOOL) fBackground; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hdc"></span><span id="HDC"></span>*cámaras*
</dt> <dd>

Identificador del controlador de dominio usado para obtener la paleta.

</dd> <dt>

<span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*
</dt> <dd>

Marca de fondo. Especifique **true** para obtener la paleta como una tarea en segundo plano o **false** para obtener la paleta en primer plano.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza la paleta de dibujo o \_ no se admite ICERR si se realiza la paleta asociada a los datos descomprimidos.

## <a name="remarks"></a>Observaciones

Los controladores deben responder a este mensaje solo si la paleta de dibujo es diferente de la paleta descomprimida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





