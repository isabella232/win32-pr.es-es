---
title: ICM_GETDEFAULTKEYFRAMERATE mensaje (Vfw.h)
description: El ICM mensaje GETDEFAULTKEYFRAMERATE consulta a un controlador de compresión de vídeo su espaciado de fotogramas clave predeterminado \_ (o preferido). Puede enviar este mensaje explícitamente o mediante la macro ICGetDefaulteyFrameRate.
ms.assetid: 2ebe37cc-3ec2-4b52-bd8f-71c44b704647
keywords:
- ICM_GETDEFAULTKEYFRAMERATE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTKEYFRAMERATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64f2796ca1c2de10222330217a0e1deb7883baa
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370597"
---
# <a name="icm_getdefaultkeyframerate-message"></a>\_ICM Mensaje GETDEFAULTKEYFRAMERATE

El **ICM \_ mensaje GETDEFAULTKEYFRAMERATE** consulta a un controlador de compresión de vídeo su espaciado de fotogramas clave predeterminado (o preferido). Puede enviar este mensaje explícitamente o mediante la macro [**ICGetDefaulteyFrameRate.**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate)


```C++
ICM_GETDEFAULTKEYFRAMERATE 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

Dirección que contiene el espaciado entre fotogramas clave preferido.

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

 

 





