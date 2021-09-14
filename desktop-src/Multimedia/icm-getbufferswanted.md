---
title: ICM_GETBUFFERSWANTED mensaje (Vfw.h)
description: El ICM mensaje GETBUFFERSWANTED consulta a un controlador el número de búferes que \_ se asignarán. Puede enviar este mensaje explícitamente o mediante la macro ICGetBuffersWanted.
ms.assetid: 109e8627-7ed4-4f17-bf7f-e77f42dfc8c7
keywords:
- ICM_GETBUFFERSWANTED mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETBUFFERSWANTED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06de8cc3bcfe463d0318651c8e2d51b269504769
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246272"
---
# <a name="icm_getbufferswanted-message"></a>\_ICM Mensaje GETBUFFERSWANTED

El **ICM \_ mensaje GETBUFFERSWANTED** consulta a un controlador el número de búferes que se asignarán. Puede enviar este mensaje explícitamente o mediante la macro [**ICGetBuffersWanted.**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted)


```C++
ICM_GETBUFFERSWANTED 
wParam = (DWORD_PTR) (LPVOID) lpdwBuffers; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*
</dt> <dd>

Dirección para contener el número de muestras que el controlador necesita para representar los datos de forma eficaz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o ICERR \_ UNSUPPORTED en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje lo usan los controladores que usan hardware para representar datos y desean garantizar un retraso de tiempo mínimo causado por la espera de que lleguen los búferes. Por ejemplo, si un controlador controla una placa de descompresión de vídeo que puede contener 10 fotogramas de vídeo, podría devolver 10 para este mensaje. Esto indica a las aplicaciones que intenten mantenerse 10 fotogramas por delante del marco que necesita actualmente.

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

 

 





