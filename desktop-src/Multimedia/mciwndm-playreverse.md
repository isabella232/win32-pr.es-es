---
title: MCIWNDM_PLAYREVERSE mensaje (Vfw.h)
description: El mensaje PLAYREVERSE de MCIWNDM reproduce el contenido actual en la dirección inversa, empezando en la posición actual y finalizando al principio del contenido o hasta que otro comando detiene la \_ reproducción.
ms.assetid: 93a22454-eca6-453f-abbe-6cf20198dbad
keywords:
- MCIWNDM_PLAYREVERSE mensaje Windows Multimedia
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
ms.openlocfilehash: f5664ea53f73745648e668a78a6dc5f6da28a9cb27d54b96fced09523f655ed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037975"
---
# <a name="mciwndm_playreverse-message"></a>Mensaje PLAYREVERSE de MCIWNDM \_

El **mensaje \_ PLAYREVERSE de MCIWNDM** reproduce el contenido actual en la dirección inversa, empezando en la posición actual y finalizando al principio del contenido o hasta que otro comando detiene la reproducción. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndPlayReverse.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)


```C++
MCIWNDM_PLAYREVERSE 
wParam = 0; 
lParam = 0; 
```



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

[**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
</dt> </dl>

 

 





