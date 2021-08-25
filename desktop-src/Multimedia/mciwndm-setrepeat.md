---
title: MCIWNDM_SETREPEAT mensaje (Vfw.h)
description: El mensaje MCIWNDM \_ SETREPEAT establece la marca de repetición asociada a la reproducción continua.
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- MCIWNDM_SETREPEAT mensaje Windows Multimedia
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
ms.openlocfilehash: 158e0b52f01431886fd8a70e89efadfdd7335258c0808cdb6780bf06071e3280
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807595"
---
# <a name="mciwndm_setrepeat-message"></a>Mensaje MCIWNDM \_ SETREPEAT

El **mensaje MCIWNDM \_ SETREPEAT** establece la marca de repetición asociada a la reproducción continua. El **mensaje MCIWNDM \_ SETREPEAT** funciona junto con el [comando MCI \_ PLAY](mci-play.md) para proporcionar un bucle de reproducción continua. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetRepeat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)


```C++
MCIWNDM_SETREPEAT 
wParam = 0; 
lParam = (LPARAM) (BOOL) f; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

Nuevo estado de la marca de repetición. Especifique **TRUE para** activar la reproducción continua.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero.

## <a name="remarks"></a>Comentarios

Actualmente, MCIAVI es el único dispositivo que admite la reproducción continua.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI \_ PLAY](mci-play.md)
</dt> <dt>

[**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 





