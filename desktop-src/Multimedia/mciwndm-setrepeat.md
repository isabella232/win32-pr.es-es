---
title: Mensaje de MCIWNDM_SETREPEAT (VFW. h)
description: El \_ mensaje MCIWNDM SETREPEAT establece la marca de repetición asociada con la reproducción continua.
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- Mensaje de MCIWNDM_SETREPEAT de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeae2ac3cb57f8ddbb2343ee3f42d30fa8def370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905414"
---
# <a name="mciwndm_setrepeat-message"></a>MCIWNDM \_ SETREPEAT

El mensaje **MCIWNDM \_ SETREPEAT** establece la marca de repetición asociada con la reproducción continua. El mensaje **MCIWNDM \_ SETREPEAT** funciona junto con el comando [MCI \_ Play](mci-play.md) para proporcionar un bucle de reproducción continuo. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) .


```C++
MCIWNDM_SETREPEAT 
wParam = 0; 
lParam = (LPARAM) (BOOL) f; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="f"></span><span id="F"></span>*formato*
</dt> <dd>

Nuevo estado de la marca de repetición. Especifique **true** para activar la reproducción continua.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero.

## <a name="remarks"></a>Observaciones

Actualmente, MCIAVI es el único dispositivo que admite la reproducción continua.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[reproducción de MCI \_](mci-play.md)
</dt> <dt>

[**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 





