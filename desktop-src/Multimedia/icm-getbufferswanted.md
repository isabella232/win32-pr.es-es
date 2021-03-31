---
title: Mensaje de ICM_GETBUFFERSWANTED (VFW. h)
description: El \_ mensaje GETBUFFERSWANTED ICM consulta a un controlador el número de búferes que se van a asignar. Puede enviar este mensaje explícitamente o mediante la macro ICGetBuffersWanted.
ms.assetid: 109e8627-7ed4-4f17-bf7f-e77f42dfc8c7
keywords:
- Mensaje de ICM_GETBUFFERSWANTED de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996053"
---
# <a name="icm_getbufferswanted-message"></a>\_Mensaje GETBUFFERSWANTED ICM

El **mensaje \_ GETBUFFERSWANTED ICM** consulta a un controlador el número de búferes que se van a asignar. Puede enviar este mensaje explícitamente o mediante la macro [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) .


```C++
ICM_GETBUFFERSWANTED 
wParam = (DWORD_PTR) (LPVOID) lpdwBuffers; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*
</dt> <dd>

Address para contener el número de muestras que el controlador necesita para representar los datos de forma eficaz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si es correcto o ICERR \_ no se admite en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje lo usan los controladores que usan Hardware para representar datos y desean garantizar un retraso mínimo causado por la espera de que lleguen los búferes. Por ejemplo, si un controlador controla una placa de descompresión de vídeo que puede contener 10 fotogramas de vídeo, podría devolver 10 para este mensaje. Esto indica a las aplicaciones que intenten mantener 10 fotogramas por encima del marco que necesita actualmente.

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

 

 





