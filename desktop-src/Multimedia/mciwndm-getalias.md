---
title: MCIWNDM_GETALIAS mensaje (Vfw.h)
description: El mensaje GETALIAS de MCIWNDM recupera el alias usado para abrir un archivo o un dispositivo \_ MCI con la función mciSendString. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetAlias.
ms.assetid: 37131b89-275c-4ab6-9278-0e08c42471bd
keywords:
- MCIWNDM_GETALIAS mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETALIAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857ea90205b5204cd7c4af19f27a420684e59543717b2689f178d97cd5a600de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137756"
---
# <a name="mciwndm_getalias-message"></a>Mensaje GETALIAS de MCIWNDM \_

El **mensaje \_ GETALIAS de MCIWNDM** recupera el alias usado para abrir un archivo o un dispositivo MCI con la [**función mciSendString.**](/previous-versions//dd757161(v=vs.85)) Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetAlias.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)


```C++
MCIWNDM_GETALIAS 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve el alias del dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**mciSendString**](/previous-versions//dd757161(v=vs.85))
</dt> <dt>

[**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)
</dt> </dl>

 

