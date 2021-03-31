---
title: Mensaje de MCIWNDM_GETMODE (VFW. h)
description: El \_ mensaje MCIWNDM GETMODE recupera el modo de funcionamiento actual de un dispositivo MCI. Los dispositivos MCI tienen varios modos operativos, que se designan mediante constantes. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetMode.
ms.assetid: cc327281-434e-4047-9e15-c04a10953f47
keywords:
- Mensaje de MCIWNDM_GETMODE de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daefea2c550a1d0cf807ae03840c38ae8b2567c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149874"
---
# <a name="mciwndm_getmode-message"></a>MCIWNDM \_ GETMODE

El mensaje **MCIWNDM \_ GETMODE** recupera el modo de funcionamiento actual de un dispositivo MCI. Los dispositivos MCI tienen varios modos operativos, que se designan mediante constantes. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) .


```C++
MCIWNDM_GETMODE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*terminado*
</dt> <dd>

Tamaño, en bytes, del búfer.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Puntero al búfer definido por la aplicación que se usa para devolver el modo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un entero que corresponde a la constante de MCI que define el modo.

## <a name="remarks"></a>Observaciones

Si la cadena terminada en null que describe el modo es más larga que el búfer, se trunca.

No todos los dispositivos pueden funcionar en todos los modos. Por ejemplo, el dispositivo MCIAVI es un dispositivo de reproducción; no es compatible con el modo de grabación. Los siguientes modos se pueden recuperar mediante **MCIWNDM \_ GETMODE**.



| Modo de funcionamiento | MCI (constante)          |
|----------------|-----------------------|
| no está listo      | \_modo MCI \_ no \_ listo |
| abrir           | \_modo MCI \_ abierto       |
| en pausa         | \_pausar modo MCI \_      |
| reproducción        | \_reproducción en modo MCI \_       |
| grabación      | \_registro en modo MCI \_     |
| buscar        | \_búsqueda en modo MCI \_       |
| stopped        | \_detención del modo MCI \_       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)
</dt> </dl>

 

 





