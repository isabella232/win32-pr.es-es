---
title: Mensaje de MCIWNDM_GETPOSITION (VFW. h)
description: El \_ mensaje MCIWNDM GETPOSITION recupera el valor numérico de la posición actual en el contenido del dispositivo MCI.
ms.assetid: 6dc5d3bd-8515-4514-a2a5-c1bee07f7acf
keywords:
- Mensaje de MCIWNDM_GETPOSITION de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETPOSITION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e7468b0e3698a72d3dce82bbd1591d59940d9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905054"
---
# <a name="mciwndm_getposition-message"></a>Mensaje de MCIWNDM \_ GETPOSITION

El mensaje **MCIWNDM \_ GETPOSITION** recupera el valor numérico de la posición actual en el contenido del dispositivo MCI. Esta macro también proporciona la posición actual en forma de cadena en un búfer definido por la aplicación. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) o [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) .


```C++
MCIWNDM_GETPOSITION 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPTSTR) lp; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*terminado*
</dt> <dd>

Tamaño, en bytes, del búfer. Si la cadena terminada en NULL es más larga que el búfer, se trunca. Use cero para impedir la recuperación de la posición como una cadena.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Puntero a un búfer definido por la aplicación que se usa para devolver la posición. Use cero para impedir la recuperación de la posición como una cadena. Si el dispositivo admite pistas, se devuelve la información de posición de cadena con el formato TT: MM: SS: FF, donde TT corresponde a las pistas, MM y SS corresponden a minutos y segundos, y FF corresponde a fotogramas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un entero que corresponde a la posición actual. Las unidades para el valor de posición dependen del formato de hora actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
</dt> <dt>

[**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
</dt> </dl>

 

 





