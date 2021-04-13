---
title: Mensaje de MCIWNDM_GETSTART (VFW. h)
description: El \_ mensaje GETSTART de MCIWNDM recupera la ubicación del inicio del contenido de un dispositivo o archivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetStart.
ms.assetid: 2350616c-2aac-4ff6-b074-bb785a97cdfb
keywords:
- Mensaje de MCIWNDM_GETSTART de Windows multimedia
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
ms.openlocfilehash: 63cbe88df006f1f98854e42259074d82bbd87dc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489418"
---
# <a name="mciwndm_getstart-message"></a>MCIWNDM \_ GETSTART

El **mensaje \_ GETSTART de MCIWNDM** recupera la ubicación del inicio del contenido de un dispositivo o archivo MCI. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) .


```C++
MCIWNDM_GETSTART 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve la ubicación en el formato de hora actual.

## <a name="remarks"></a>Observaciones

Normalmente, el valor devuelto es cero; pero algunos dispositivos usan una ubicación de inicio distinto de cero. Al buscar en esta ubicación, el dispositivo se establece en el inicio del medio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
</dt> </dl>

 

 





