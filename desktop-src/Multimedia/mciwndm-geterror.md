---
title: MCIWNDM_GETERROR mensaje (Vfw.h)
description: El mensaje GETERROR de MCIWNDM \_ recupera el último error de MCI encontrado. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetError.
ms.assetid: f110a9b3-5b05-4bf0-85d1-b49ce7396222
keywords:
- MCIWNDM_GETERROR mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c2977bb079351824b48da21f4ba3cc2dc5afe7e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370651"
---
# <a name="mciwndm_geterror-message"></a>Mensaje GETERROR de MCIWNDM \_

El **mensaje \_ GETERROR de MCIWNDM** recupera el último error de MCI encontrado. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetError.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)


```C++
MCIWNDM_GETERROR 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Tamaño, en bytes, del búfer de errores.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Puntero a un búfer definido por la aplicación que se usa para devolver la cadena de error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de error entero si se realiza correctamente.

## <a name="remarks"></a>Observaciones

Si *lp* es un puntero válido, se devuelve una cadena terminada en NULL correspondiente al error en su búfer. Si la cadena de error es mayor que el búfer, MCIWnd la trunca.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
</dt> </dl>

 

 





