---
title: Mensaje de MCIWNDM_VALIDATEMEDIA (VFW. h)
description: El \_ mensaje MCIWNDM VALIDATEMEDIA actualiza las ubicaciones inicial y final del contenido, la posición actual en el contenido y el TrackBar según el formato de hora actual.
ms.assetid: 98ac6227-fc90-4276-8e26-2bd005e35dc6
keywords:
- Mensaje de MCIWNDM_VALIDATEMEDIA de Windows multimedia
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
ms.openlocfilehash: 43cb6e6a4a7c320d4eb6472c3c72da2843d0814c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533796"
---
# <a name="mciwndm_validatemedia-message"></a>MCIWNDM \_ VALIDATEMEDIA

El mensaje **MCIWNDM \_ VALIDATEMEDIA** actualiza las ubicaciones inicial y final del contenido, la posición actual en el contenido y el TrackBar según el formato de hora actual. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) .


```C++
MCIWNDM_VALIDATEMEDIA 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Normalmente, no es necesario usar esta macro; sin embargo, si la aplicación cambia el formato de hora de un dispositivo sin usar MCIWnd; las ubicaciones inicial y final del contenido, así como la barra de inicio, siguen usando el formato antiguo. Puede usar esta macro para actualizar estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)
</dt> </dl>

 

 





