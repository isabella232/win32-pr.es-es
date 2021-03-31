---
title: Mensaje de MCIWNDM_PLAYREVERSE (VFW. h)
description: El \_ mensaje MCIWNDM PLAYREVERSE reproduce el contenido actual en dirección inversa, comenzando en la posición actual y terminando al principio del contenido o hasta que otro comando detenga la reproducción.
ms.assetid: 93a22454-eca6-453f-abbe-6cf20198dbad
keywords:
- Mensaje de MCIWNDM_PLAYREVERSE de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYREVERSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b0a2e230e3c57e8314e455be5dfbc5cea2c013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149873"
---
# <a name="mciwndm_playreverse-message"></a>MCIWNDM \_ PLAYREVERSE

El mensaje **MCIWNDM \_ PLAYREVERSE** reproduce el contenido actual en dirección inversa, comenzando en la posición actual y terminando al principio del contenido o hasta que otro comando detenga la reproducción. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) .


```C++
MCIWNDM_PLAYREVERSE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
</dt> </dl>

 

 





