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
ms.openlocfilehash: 84b0a2e230e3c57e8314e455be5dfbc5cea2c013
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250815"
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

 

 





