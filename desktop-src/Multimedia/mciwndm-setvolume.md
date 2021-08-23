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
ms.openlocfilehash: e8c40d2c8b2c7c4cb309b5c6e5b21dcd29e6c8ee27b9ca8c97556cb14927a121
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428545"
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

Devuelve cero si se realiza correctamente o un error en caso contrario.

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

 

 





