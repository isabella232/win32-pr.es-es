---
title: MCIWNDM_GETTIMEFORMAT mensaje (Vfw.h)
description: El mensaje GETTIMEFORMAT de MCIWNDM recupera el formato de hora actual de un dispositivo MCI en dos formas como un valor numérico y \_ como una cadena. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetTimeFormat.
ms.assetid: 01844872-5444-4f3b-92a3-64f80b94d3a0
keywords:
- MCIWNDM_GETTIMEFORMAT mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370682"
---
# <a name="mciwndm_gettimeformat-message"></a>Mensaje GETTIMEFORMAT de MCIWNDM \_

El **mensaje \_ GETTIMEFORMAT de MCIWNDM** recupera el formato de hora actual de un dispositivo MCI de dos formas: como un valor numérico y como una cadena. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetTimeFormat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)


```C++
MCIWNDM_GETTIMEFORMAT 
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

Puntero a un búfer que contiene la forma de cadena terminada en NULL del formato de hora.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un entero correspondiente a la constante MCI que define el formato de hora.

## <a name="remarks"></a>Observaciones

Si la cadena de formato de hora es mayor que el búfer devuelto, MCIWnd trunca la cadena.

Un dispositivo MCI puede admitir uno o varios de los siguientes formatos de hora.



| Formato de hora                      | Constante MCI               |
|----------------------------------|----------------------------|
| Bytes                            | BYTES DE FORMATO MCI \_ \_         |
| Marcos                           | MARCOS DE FORMATO MCI \_ \_        |
| Horas, minutos, segundos          | MCI \_ FORMAT \_ HMS           |
| Milisegundos                     | MILISEGUNDOS DE FORMATO MCI \_ \_  |
| Minutos, segundos, fotogramas         | MCI \_ FORMAT \_ MSF           |
| Ejemplos                          | EJEMPLOS DE FORMATO \_ MCI \_       |
| SMPTE 24                         | MCI \_ FORMAT \_ SMPTE \_ 24     |
| SMPTE 25                         | MCI \_ FORMAT \_ SMPTE \_ 25     |
| SMPTE 30 drop                    | MCI \_ FORMAT \_ SMPTE \_ 30DROP |
| SMPTE 30 (sin quitar)              | MCI \_ FORMAT \_ SMPTE \_ 30     |
| Seguimientos, minutos, segundos, fotogramas | \_TMSF CON \_ FORMATO MCI          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> </dl>

 

 





