---
title: ICM_DRAW_REALIZE mensaje (Vfw.h)
description: El ICM DRAW REALIZE notifica a un controlador de representación \_ que se dé cuenta de su paleta de dibujo durante el \_ dibujo. Puede enviar este mensaje explícitamente o mediante la macro ICDrawRealize.
ms.assetid: 501540cd-41e2-4f80-abf8-2ec2179970a9
keywords:
- ICM_DRAW_REALIZE mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370556"
---
# <a name="icm_draw_realize-message"></a>\_ICM Mensaje DRAW \_ REALIZE

El **ICM \_ DRAW \_ REALIZE** notifica a un controlador de representación que se dé cuenta de su paleta de dibujo durante el dibujo. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawRealize.**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize)


```C++
ICM_DRAW_REALIZE 
wParam = (DWORD_PTR) (UINT_PTR) (HDC) hdc; 
lParam = (DWORD_PTR) (BOOL) fBackground; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hdc"></span><span id="HDC"></span>*Hdc*
</dt> <dd>

Identificador del controlador de dominio que se usa para realizar la paleta.

</dd> <dt>

<span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*
</dt> <dd>

Marca de fondo. Especifique **TRUE para** realizar la paleta como una tarea de fondo o **FALSE** para realizar la paleta en primer plano.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR OK si se realiza la paleta de dibujo o ICERR UNSUPPORTED si se realiza la paleta asociada a los datos \_ \_ descomprimidos.

## <a name="remarks"></a>Observaciones

Los controladores solo deben responder a este mensaje si la paleta de dibujo es diferente de la paleta descomprimida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





