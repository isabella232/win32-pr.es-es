---
title: MCIWNDM_GETLENGTH mensaje (Vfw.h)
description: El mensaje GETLENGTH de MCIWNDM recupera la longitud del contenido o archivo usado actualmente \_ por un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetLength.
ms.assetid: bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f
keywords:
- MCIWNDM_GETLENGTH mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETLENGTH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334d9a4a62171a62cbd0fc914be2d9a81ed901eab6d3893170cb8dabd2426a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374192"
---
# <a name="mciwndm_getlength-message"></a>Mensaje GETLENGTH de MCIWNDM \_

El **mensaje \_ GETLENGTH de MCIWNDM** recupera la longitud del contenido o archivo usado actualmente por un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetLength.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)


```C++
MCIWNDM_GETLENGTH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve la longitud. Las unidades para la longitud dependen del formato de hora actual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
</dt> </dl>

 

 





