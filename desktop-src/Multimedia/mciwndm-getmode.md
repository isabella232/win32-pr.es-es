---
title: MCIWNDM_GETMODE mensaje (Vfw.h)
description: El mensaje GETMODE de MCIWNDM \_ recupera el modo de funcionamiento actual de un dispositivo MCI. Los dispositivos MCI tienen varios modos de funcionamiento, que se designan mediante constantes. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetMode.
ms.assetid: cc327281-434e-4047-9e15-c04a10953f47
keywords:
- MCIWNDM_GETMODE mensaje Windows Multimedia
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
ms.openlocfilehash: 645d7a660df8d22cb2adb70a775d5431eb31dc986b502bb4dbb36b1963ce06f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429276"
---
# <a name="mciwndm_getmode-message"></a>Mensaje GETMODE de MCIWNDM \_

El **mensaje \_ GETMODE de MCIWNDM** recupera el modo de funcionamiento actual de un dispositivo MCI. Los dispositivos MCI tienen varios modos de funcionamiento, que se designan mediante constantes. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetMode.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)


```C++
MCIWNDM_GETMODE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Tamaño, en bytes, del búfer.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Puntero al búfer definido por la aplicación que se usa para devolver el modo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un entero correspondiente a la constante MCI que define el modo.

## <a name="remarks"></a>Observaciones

Si la cadena terminada en NULL que describe el modo es mayor que el búfer, se trunca.

No todos los dispositivos pueden funcionar en todos los modo. Por ejemplo, el dispositivo MCIAVI es un dispositivo de reproducción; no admite el modo de grabación. Los modos siguientes se pueden recuperar mediante **MCIWNDM \_ GETMODE**.



| Modo de funcionamiento | Constante MCI          |
|----------------|-----------------------|
| no está listo      | MODO MCI \_ \_ NO \_ LISTO |
| abierto           | MODO MCI \_ \_ ABIERTO       |
| en pausa         | PAUSA DEL MODO MCI \_ \_      |
| reproducción        | REPRODUCCIÓN EN MODO MCI \_ \_       |
| grabación      | REGISTRO DEL MODO MCI \_ \_     |
| buscar        | MCI \_ MODE \_ SEEK       |
| stopped        | MCI \_ MODE \_ STOP       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)
</dt> </dl>

 

 





