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
ms.openlocfilehash: 2c0fa1b3f4b3359e1609b3ba12009fe5879c304a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250820"
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

## <a name="remarks"></a>Observaciones

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

 

 





