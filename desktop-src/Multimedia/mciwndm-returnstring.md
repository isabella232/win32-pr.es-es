---
title: MCIWNDM_RETURNSTRING mensaje (Vfw.h)
description: El mensaje MCIWNDM RETURNSTRING recupera la respuesta al comando de cadena MCI más reciente enviado \_ a un dispositivo MCI.
ms.assetid: 36a5222c-a63c-4b8c-ad0c-a00477e95b96
keywords:
- MCIWNDM_RETURNSTRING mensaje Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250772"
---
# <a name="mciwndm_returnstring-message"></a>Mensaje RETURNSTRING de MCIWNDM \_

El **mensaje MCIWNDM \_ RETURNSTRING** recupera la respuesta al comando de cadena MCI más reciente enviado a un dispositivo MCI. La información de la respuesta se proporciona como una cadena terminada en NULL. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndReturnString.**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)


```C++
MCIWNDM_RETURNSTRING 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Tamaño, en bytes, del búfer.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Puntero a un búfer definido por la aplicación que contiene la cadena terminada en NULL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un entero correspondiente a la cadena MCI.

## <a name="remarks"></a>Observaciones

Si la cadena terminada en NULL es mayor que el búfer, la cadena se trunca.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
</dt> </dl>

 

 





