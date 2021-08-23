---
title: ICM_GETDEFAULTQUALITY mensaje (Vfw.h)
description: El ICM mensaje GETDEFAULTQUALITY consulta un controlador de compresión \_ de vídeo para proporcionar su configuración de calidad predeterminada. Puede enviar este mensaje explícitamente o mediante la macro ICGetDefaultQuality.
ms.assetid: bba7f451-52c2-4684-a7c9-e4b05cb946c5
keywords:
- ICM_GETDEFAULTQUALITY mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df9c27527cea53c4b4eca6cf75babef3a41f80732d8ecf7a18528c07d6d9311b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525915"
---
# <a name="icm_getdefaultquality-message"></a>\_ICM Mensaje GETDEFAULTQUALITY

El **ICM \_ mensaje GETDEFAULTQUALITY** consulta un controlador de compresión de vídeo para proporcionar su configuración de calidad predeterminada. Puede enviar este mensaje explícitamente o mediante la macro [**ICGetDefaultQuality.**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality)


```C++
ICM_GETDEFAULTQUALITY 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

Dirección que contiene el valor de calidad predeterminado. Los valores de calidad oscilan entre 0 y 10 000.

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

 

 





