---
title: Mensaje de MCIWNDM_RETURNSTRING (VFW. h)
description: El \_ mensaje RETURNSTRING de MCIWNDM recupera la respuesta al comando de cadena MCI más reciente enviado a un dispositivo MCI.
ms.assetid: 36a5222c-a63c-4b8c-ad0c-a00477e95b96
keywords:
- Mensaje de MCIWNDM_RETURNSTRING de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_RETURNSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b99307bd7d61a70db594d0a696cceccd6d246a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079344"
---
# <a name="mciwndm_returnstring-message"></a>MCIWNDM \_ RETURNSTRING

El **mensaje \_ RETURNSTRING de MCIWNDM** recupera la respuesta al comando de cadena MCI más reciente enviado a un dispositivo MCI. La información de la respuesta se proporciona como una cadena terminada en NULL. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .


```C++
MCIWNDM_RETURNSTRING 
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

Puntero a un búfer definido por la aplicación que va a contener la cadena terminada en NULL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un entero que corresponde a la cadena MCI.

## <a name="remarks"></a>Observaciones

Si la cadena terminada en NULL es más larga que el búfer, la cadena se trunca.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
</dt> </dl>

 

 





