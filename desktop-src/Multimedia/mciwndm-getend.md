---
title: Mensaje de MCIWNDM_GETEND (VFW. h)
description: El \_ mensaje MCIWNDM GETEND recupera la ubicación del final del contenido de un dispositivo MCI o un archivo. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetEnd.
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- Mensaje de MCIWNDM_GETEND de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETEND
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d18057619e31fa9b22d7f6354527c394c02798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905570"
---
# <a name="mciwndm_getend-message"></a>MCIWNDM \_ GETEND

El mensaje **MCIWNDM \_ GETEND** recupera la ubicación del final del contenido de un dispositivo MCI o un archivo. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) .


```C++
MCIWNDM_GETEND 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve la ubicación en el formato de hora actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
</dt> </dl>

 

 





