---
title: Mensaje de MCIWNDM_PLAYTO (VFW. h)
description: El \_ mensaje MCIWNDM playto reproduce el contenido de un dispositivo MCI desde la posición actual hasta la ubicación final especificada o hasta que otro comando detiene la reproducción.
ms.assetid: ed940ee7-7b96-47da-99d3-6697f8a2e3d5
keywords:
- Mensaje de MCIWNDM_PLAYTO de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150869"
---
# <a name="mciwndm_playto-message"></a>Mensaje de MCIWNDM \_ playto

El mensaje **MCIWNDM \_ playto** reproduce el contenido de un dispositivo MCI desde la posición actual hasta la ubicación final especificada o hasta que otro comando detiene la reproducción. Si la ubicación de finalización especificada está más allá del final del contenido, la reproducción se detiene al final del contenido. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) .


```C++
MCIWNDM_PLAYTO 
wParam = 0; 
lParam = (LPARAM) (LONG) lEnd; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*Acreedor*
</dt> <dd>

Ubicación final. Las unidades de la ubicación de finalización dependen del formato de hora actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Esta macro se define mediante las macros [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) y [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) , que a su vez usan el comando [MCI \_ Seek](mci-seek.md) y el mensaje **MCIWNDM \_ playto** .

También puede especificar una ubicación inicial y final para la reproducción mediante la macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[búsqueda de MCI \_](mci-seek.md)
</dt> <dt>

[**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> <dt>

[**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
</dt> <dt>

[**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
</dt> </dl>

 

 





