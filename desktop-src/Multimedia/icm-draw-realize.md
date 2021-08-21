---
title: ICM_DRAW_REALIZE mensaje (Vfw.h)
description: El ICM DRAW REALIZE notifica a un \_ controlador de representación que se dé cuenta de su paleta de dibujos durante el \_ dibujo. Puede enviar este mensaje explícitamente o mediante la macro ICDrawRealize.
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
ms.openlocfilehash: f05e9bd21cc8185afd17ec909fcf95bf3ac6bedba7477f47191b9f3d51383914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987250"
---
# <a name="icm_draw_realize-message"></a>\_ICM Mensaje DRAW \_ REALIZE

El **ICM \_ DRAW \_ REALIZE** notifica a un controlador de representación que se dé cuenta de su paleta de dibujos durante el dibujo. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawRealize.**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize)


```C++
ICM_DRAW_REALIZE 
wParam = (DWORD_PTR) (UINT_PTR) (HDC) hdc; 
lParam = (DWORD_PTR) (BOOL) fBackground; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hdc"></span><span id="HDC"></span>*Hdc*
</dt> <dd>

Identificador del controlador de dominio utilizado para realizar la paleta.

</dd> <dt>

<span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*
</dt> <dd>

Marca de fondo. Especifique **TRUE** para realizar la paleta como una tarea de fondo o **FALSE** para realizar la paleta en primer plano.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR OK si se realiza la paleta de dibujos o ICERR UNSUPPORTED si se realiza la paleta asociada a los datos \_ \_ descomprimidos.

## <a name="remarks"></a>Comentarios

Los controladores solo deben responder a este mensaje si la paleta de dibujos es diferente de la paleta descomprimida.

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

 

 





