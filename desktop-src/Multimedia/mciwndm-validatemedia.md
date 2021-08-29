---
title: MCIWNDM_VALIDATEMEDIA mensaje (Vfw.h)
description: El mensaje VALIDATEMEDIA de MCIWNDM actualiza las ubicaciones inicial y final del contenido, la posición actual en el contenido y la barra de seguimiento según el \_ formato de hora actual.
ms.assetid: 98ac6227-fc90-4276-8e26-2bd005e35dc6
keywords:
- MCIWNDM_VALIDATEMEDIA mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_VALIDATEMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2db79f5714a9f48a2fdd73ff6eedecd0a14172e352e0a40ffbdccdd3aaaf4c2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428535"
---
# <a name="mciwndm_validatemedia-message"></a>Mensaje VALIDATEMEDIA de MCIWNDM \_

El **mensaje \_ VALIDATEMEDIA de MCIWNDM** actualiza las ubicaciones inicial y final del contenido, la posición actual en el contenido y la barra de seguimiento según el formato de hora actual. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndValidateMedia.**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)


```C++
MCIWNDM_VALIDATEMEDIA 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

Normalmente, no es necesario usar esta macro; sin embargo, si la aplicación cambia el formato de hora de un dispositivo sin usar MCIWnd; las ubicaciones inicial y final del contenido, así como la barra de seguimiento, siguen usando el formato anterior. Puede usar esta macro para actualizar estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)
</dt> </dl>

 

 





