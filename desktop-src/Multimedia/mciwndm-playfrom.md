---
title: MCIWNDM_PLAYFROM mensaje (Vfw.h)
description: El mensaje MCIWNDM PLAYFROM reproduce el contenido de un dispositivo MCI desde la ubicación especificada hasta el final del contenido o hasta que otro comando \_ detiene la reproducción. Puede enviar este mensaje explícitamente o mediante la macro MCIWndPlayFrom.
ms.assetid: 1c47f8eb-2a1b-4671-a9f8-fd6d59a5c7c6
keywords:
- MCIWNDM_PLAYFROM mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYFROM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67f9f2885b67f82c2285bcaacb395c626dbe460800a2683f72dad0730999e843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037995"
---
# <a name="mciwndm_playfrom-message"></a>Mensaje MCIWNDM \_ PLAYFROM

El **mensaje MCIWNDM \_ PLAYFROM** reproduce el contenido de un dispositivo MCI desde la ubicación especificada hasta el final del contenido o hasta que otro comando detiene la reproducción. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndPlayFrom.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)


```C++
MCIWNDM_PLAYFROM 
wParam = 0; 
lParam = (LPARAM) (LONG) lPos; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*lPos*
</dt> <dd>

Ubicación inicial. Las unidades de la ubicación inicial dependen del formato de hora actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

También puede especificar una ubicación inicial y final para la reproducción mediante la macro [**MCIWndPlayFromTo.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
</dt> <dt>

[**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> </dl>

 

 





