---
title: MCIWNDM_PLAYTO mensaje (Vfw.h)
description: El mensaje MCIWNDM PLAYTO reproduce el contenido de un dispositivo MCI desde la posición actual hasta la ubicación final especificada o hasta que otro \_ comando detiene la reproducción.
ms.assetid: ed940ee7-7b96-47da-99d3-6697f8a2e3d5
keywords:
- MCIWNDM_PLAYTO mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYTO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf0104204dc0306615ead91be036459cdf3c11d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370724"
---
# <a name="mciwndm_playto-message"></a>Mensaje PLAYTO de MCIWNDM \_

El **mensaje MCIWNDM \_ PLAYTO** reproduce el contenido de un dispositivo MCI desde la posición actual hasta la ubicación final especificada o hasta que otro comando detiene la reproducción. Si la ubicación final especificada está más allá del final del contenido, la reproducción se detiene al final del contenido. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndPlayTo.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)


```C++
MCIWNDM_PLAYTO 
wParam = 0; 
lParam = (LPARAM) (LONG) lEnd; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*Prestar*
</dt> <dd>

Ubicación final. Las unidades de la ubicación final dependen del formato de hora actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Esta macro se define mediante las macros [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) y [**MCIWndPlayTo,**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) que a su vez usan el comando [MCI \_ SEEK](mci-seek.md) y el mensaje **MCIWNDM \_ PLAYTO.**

También puede especificar una ubicación inicial y final para la reproducción mediante la macro [**MCIWndPlayFromTo.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI \_ SEEK](mci-seek.md)
</dt> <dt>

[**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> <dt>

[**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
</dt> <dt>

[**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
</dt> </dl>

 

 





