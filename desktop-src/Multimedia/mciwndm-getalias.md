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
ms.openlocfilehash: 9e971c50b9abc450387ac29f9a7331bfdca5c38c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476799"
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



| Requisito | Value |
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

 

