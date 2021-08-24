---
title: MCIWNDM_GETSTYLES mensaje (Vfw.h)
description: El mensaje GETSTYLES de MCIWNDM recupera las marcas que especifican los estilos de \_ ventana MCIWnd actuales usados por una ventana. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetStyles.
ms.assetid: cd34ba05-47cb-488e-a6c6-4ec1c0d25de8
keywords:
- MCIWNDM_GETSTYLES mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 036bd687c5d7828fade23994b9141488354added5ee38d38bafc9c5ce22a954c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783295"
---
# <a name="mciwndm_getstyles-message"></a>Mensaje GETSTYLES de MCIWNDM \_

El **mensaje \_ GETSTYLES de MCIWNDM** recupera las marcas que especifican los estilos de ventana MCIWnd actuales usados por una ventana. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetStyles.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)


```C++
MCIWNDM_GETSTYLES 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve un valor que representa los estilos actuales de la ventana MCIWnd. El valor devuelto es el operador OR bit a bit de los estilos de ventana MCIWnd (marcas MCIWNDF).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
</dt> </dl>

 

 





