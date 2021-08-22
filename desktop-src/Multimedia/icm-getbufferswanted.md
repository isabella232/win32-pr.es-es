---
title: ICM_GETBUFFERSWANTED mensaje (Vfw.h)
description: El ICM \_ mensaje GETBUFFERSWANTED consulta a un controlador el número de búferes que se asignarán. Puede enviar este mensaje explícitamente o mediante la macro ICGetBuffersWanted.
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
ms.openlocfilehash: c4bd5fae6e9f008649366cf922ef117f5b6f7560a7764c4f8d81552a255de48a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495875"
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

## <a name="remarks"></a>Comentarios

Este mensaje lo usan los controladores que usan hardware para representar los datos y quieren garantizar un retraso de tiempo mínimo causado por la espera de que lleguen los búferes. Por ejemplo, si un controlador controla una placa de descompresión de vídeo que puede contener 10 fotogramas de vídeo, podría devolver 10 para este mensaje. Esto indica a las aplicaciones que intenten mantener 10 fotogramas por delante del marco que necesita actualmente.

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

 

 





