---
title: Mensaje de MCIWNDM_GETTIMEFORMAT (VFW. h)
description: El \_ mensaje MCIWNDM GETTIMEFORMAT recupera el formato de hora actual de un dispositivo MCI en dos formatos como un valor numérico y como una cadena. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetTimeFormat.
ms.assetid: 01844872-5444-4f3b-92a3-64f80b94d3a0
keywords:
- Mensaje de MCIWNDM_GETTIMEFORMAT de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a09f969c009ff23bc0951ed2efbc0dbf7aa95dda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801328"
---
# <a name="mciwndm_gettimeformat-message"></a>MCIWNDM \_ GETTIMEFORMAT

El mensaje **MCIWNDM \_ GETTIMEFORMAT** recupera el formato de hora actual de un dispositivo MCI en dos formatos: como valor numérico y como cadena. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .


```C++
MCIWNDM_GETTIMEFORMAT 
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

Puntero a un búfer que va a contener la forma de cadena terminada en NULL del formato de hora.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un entero que corresponde a la constante de MCI que define el formato de hora.

## <a name="remarks"></a>Observaciones

Si la cadena de formato de hora es mayor que el búfer de retorno, MCIWnd trunca la cadena.

Un dispositivo MCI puede admitir uno o varios de los siguientes formatos de hora.



| Formato de hora                      | MCI (constante)               |
|----------------------------------|----------------------------|
| Bytes                            | \_bytes de formato de MCI \_         |
| Imágenes                           | \_marcos de formato MCI \_        |
| Horas, minutos, segundos          | \_formato MCI \_ HMS           |
| Milisegundos                     | formato MCI en \_ \_ milisegundos  |
| Minutos, segundos, fotogramas         | \_formato MCI \_ MSF           |
| Ejemplos                          | \_ejemplos de formato de MCI \_       |
| SMPTE 24                         | \_Formato MCI \_ SMPTE \_ 24     |
| SMPTE 25                         | \_Formato MCI \_ SMPTE \_ 25     |
| Eliminación SMPTE 30                    | \_Formato MCI \_ SMPTE \_ 30DROP |
| SMPTE 30 (no Drop)              | \_Formato MCI \_ SMPTE \_ 30     |
| Pistas, minutos, segundos, fotogramas | \_formato MCI \_ TMSF          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> </dl>

 

 





