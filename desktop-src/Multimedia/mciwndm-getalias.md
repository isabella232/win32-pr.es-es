---
title: Mensaje de MCIWNDM_GETALIAS (VFW. h)
description: El \_ mensaje MCIWNDM GETALIAS recupera el alias usado para abrir un dispositivo MCI o un archivo con la función mciSendString. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetAlias.
ms.assetid: 37131b89-275c-4ab6-9278-0e08c42471bd
keywords:
- Mensaje de MCIWNDM_GETALIAS de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676592"
---
# <a name="mciwndm_getalias-message"></a>MCIWNDM \_ GETALIAS

El mensaje **MCIWNDM \_ GETALIAS** recupera el alias usado para abrir un dispositivo MCI o un archivo con la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) . Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) .


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
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**mciSendString**](/previous-versions//dd757161(v=vs.85))
</dt> <dt>

[**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)
</dt> </dl>

 

