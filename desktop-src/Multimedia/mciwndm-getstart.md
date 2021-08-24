---
title: MCIWNDM_GETSTART mensaje (Vfw.h)
description: El mensaje GETSTART de MCIWNDM recupera la ubicación del principio del contenido de un archivo o \_ dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetStart.
ms.assetid: 2350616c-2aac-4ff6-b074-bb785a97cdfb
keywords:
- MCIWNDM_GETSTART mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTART
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0efb5689009fdd6928afd1d2f232bcb1bbeb2160aecf3d79ddb263ed6f315de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429235"
---
# <a name="mciwndm_getstart-message"></a>Mensaje GETSTART de MCIWNDM \_

El **mensaje \_ GETSTART de MCIWNDM** recupera la ubicación del principio del contenido de un archivo o dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetStart.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)


```C++
MCIWNDM_GETSTART 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve la ubicación en el formato de hora actual.

## <a name="remarks"></a>Observaciones

Normalmente, el valor devuelto es cero; pero algunos dispositivos usan una ubicación de inicio distinta de cero. Al buscar en esta ubicación, el dispositivo se establece en el inicio del medio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
</dt> </dl>

 

 





