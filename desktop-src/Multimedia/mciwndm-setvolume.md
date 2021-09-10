---
title: MCIWNDM_SETVOLUME mensaje (Vfw.h)
description: El mensaje SETVOLUME de MCIWNDM \_ establece el nivel de volumen de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSetVolume.
ms.assetid: 04151588-b761-447a-9a57-808c034c3059
keywords:
- MCIWNDM_SETVOLUME mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2215f8df3ea6f7b36b224318ebac68175ff9c265
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370765"
---
# <a name="mciwndm_setvolume-message"></a>Mensaje SETVOLUME de MCIWNDM \_

El **mensaje \_ SETVOLUME de MCIWNDM** establece el nivel de volumen de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetVolume.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)


```C++
MCIWNDM_SETVOLUME 
wParam = 0; 
lParam = (LPARAM) (UINT) iVol; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*Ivol*
</dt> <dd>

Nuevo nivel de volumen. Especifique 1000 para el nivel de volumen normal. Especifique un valor mayor para un volumen más alto o un valor inferior para un volumen más silencioso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
</dt> </dl>

 

 





