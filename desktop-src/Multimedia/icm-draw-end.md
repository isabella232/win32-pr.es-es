---
title: Mensaje de ICM_DRAW_END (VFW. h)
description: El \_ mensaje de \_ finalización del dibujo ICM notifica a un controlador de representación que descomprima la imagen actual en la pantalla y libere los recursos asignados para la descompresión y el dibujo. Puede enviar este mensaje explícitamente o mediante la macro ICDrawEnd.
ms.assetid: 03910752-6122-4a5a-84ff-2cecf66cf439
keywords:
- Mensaje de ICM_DRAW_END de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e420ac37791bc6c5aa7f660d71005be65fc87fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802623"
---
# <a name="icm_draw_end-message"></a>\_Mensaje final de Draw ICM \_

El mensaje de **\_ \_ finalización del dibujo ICM** notifica a un controlador de representación que descomprima la imagen actual en la pantalla y libere los recursos asignados para la descompresión y el dibujo. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) .


```C++
ICM_DRAW_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Los mensajes de [**\_ \_ Inicio de dibujo de ICM**](icm-draw-begin.md) y **\_ \_ fin de dibujo de ICM** no se anidan. Si el controlador recibe **el \_ \_ Inicio de Draw de ICM** antes de que se detenga la descompresión con el **\_ \_ extremo de Draw ICM**, debe reiniciar la descompresión con nuevos parámetros.

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

 

 





