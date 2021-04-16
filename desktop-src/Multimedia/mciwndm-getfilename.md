---
title: Mensaje de MCIWNDM_GETFILENAME (VFW. h)
description: El mensaje de MCIWNDM \_ GETFILENAME recupera el nombre de archivo que usa actualmente un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetFileName.
ms.assetid: d61b1b6d-0fae-4732-993c-41e08a4e05be
keywords:
- Mensaje de MCIWNDM_GETFILENAME de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETFILENAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 232a1d829b5cdd6da23e7dd3fb0294b95ca79f4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533813"
---
# <a name="mciwndm_getfilename-message"></a>Mensaje de MCIWNDM \_ GETFILENAME

El mensaje de **MCIWNDM \_ GETFILENAME** recupera el nombre de archivo que usa actualmente un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) .


```C++
MCIWNDM_GETFILENAME 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*terminado*
</dt> <dd>

Tamaño, en bytes, del búfer.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Puntero a un búfer definido por la aplicación para devolver el nombre de archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o 1 en caso contrario.

## <a name="remarks"></a>Observaciones

Si la cadena terminada en null que contiene el nombre de archivo es más larga que el búfer, MCIWnd trunca el nombre de archivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename)
</dt> </dl>

 

 





