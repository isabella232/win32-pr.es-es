---
title: Mensaje de ICM_GETDEFAULTKEYFRAMERATE (VFW. h)
description: El \_ mensaje GETDEFAULTKEYFRAMERATE ICM consulta un controlador de compresión de vídeo para obtener el espaciado de fotogramas clave predeterminado (o preferido). Puede enviar este mensaje explícitamente o mediante la macro ICGetDefaulteyFrameRate.
ms.assetid: 2ebe37cc-3ec2-4b52-bd8f-71c44b704647
keywords:
- Mensaje de ICM_GETDEFAULTKEYFRAMERATE de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422369"
---
# <a name="icm_getdefaultkeyframerate-message"></a>\_Mensaje GETDEFAULTKEYFRAMERATE ICM

El **mensaje \_ GETDEFAULTKEYFRAMERATE ICM** consulta un controlador de compresión de vídeo para obtener el espaciado de fotogramas clave predeterminado (o preferido). Puede enviar este mensaje explícitamente o mediante la macro [**ICGetDefaulteyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) .


```C++
ICM_GETDEFAULTKEYFRAMERATE 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

Dirección que va a contener el espaciado de fotogramas de clave preferido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si el controlador admite este mensaje o ICERR \_ no se admite en caso contrario.

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

 

 





