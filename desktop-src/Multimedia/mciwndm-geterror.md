---
title: Mensaje de MCIWNDM_GETERROR (VFW. h)
description: El \_ mensaje MCIWNDM GETERROR recupera el último error de MCI encontrado. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetError.
ms.assetid: f110a9b3-5b05-4bf0-85d1-b49ce7396222
keywords:
- Mensaje de MCIWNDM_GETERROR de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905055"
---
# <a name="mciwndm_geterror-message"></a>MCIWNDM \_ GETERROR

El mensaje **MCIWNDM \_ GETERROR** recupera el último error de MCI encontrado. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) .


```C++
MCIWNDM_GETERROR 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*terminado*
</dt> <dd>

Tamaño, en bytes, del búfer de errores.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Puntero a un búfer definido por la aplicación que se usa para devolver la cadena de error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de error de entero si se realiza correctamente.

## <a name="remarks"></a>Observaciones

Si *LP* es un puntero válido, se devuelve en su búfer una cadena terminada en NULL correspondiente al error. Si la cadena de error es más larga que el búfer, MCIWnd lo trunca.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
</dt> </dl>

 

 





