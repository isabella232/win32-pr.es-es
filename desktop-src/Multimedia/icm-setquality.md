---
title: ICM_SETQUALITY mensaje (Vfw.h)
description: El ICM \_ SETQUALITY proporciona un controlador de compresión de vídeo con un nivel de calidad para usar durante la compresión.
ms.assetid: 487ff1de-7178-440a-b38d-0b82a30d7297
keywords:
- ICM_SETQUALITY mensaje Windows multimedia
topic_type:
- apiref
api_name:
- ICM_SETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adb840b3dc283d0cd81b4662322e0571b8e687bbdd4b6e7009a6fa1786e95920
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784915"
---
# <a name="icm_setquality-message"></a>\_ICM Mensaje SETQUALITY

El **ICM \_ setquality proporciona** un controlador de compresión de vídeo con un nivel de calidad para usar durante la compresión.


```C++
ICM_SETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

Nuevo valor de calidad. Los valores de calidad oscilan entre 0 y 10 000.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si el controlador admite este mensaje o ICERR \_ UNSUPPORTED en caso contrario.

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

 

 





