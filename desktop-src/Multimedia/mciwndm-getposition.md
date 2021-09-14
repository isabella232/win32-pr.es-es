---
title: MCIWNDM_GETPOSITION mensaje (Vfw.h)
description: El mensaje GETPOSITION de MCIWNDM recupera el valor numérico de la posición actual dentro \_ del contenido del dispositivo MCI.
ms.assetid: 6dc5d3bd-8515-4514-a2a5-c1bee07f7acf
keywords:
- MCIWNDM_GETPOSITION mensaje Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069507"
---
# <a name="mciwndm_getposition-message"></a>Mensaje GETPOSITION de MCIWNDM \_

El **mensaje \_ GETPOSITION de MCIWNDM** recupera el valor numérico de la posición actual dentro del contenido del dispositivo MCI. Esta macro también proporciona la posición actual en forma de cadena en un búfer definido por la aplicación. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) o [**MCIWndGetPositionString.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)


```C++
MCIWNDM_GETPOSITION 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPTSTR) lp; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Tamaño, en bytes, del búfer. Si la cadena terminada en NULL es mayor que el búfer, se trunca. Use cero para impedir la recuperación de la posición como una cadena.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Puntero a un búfer definido por la aplicación que se usa para devolver la posición. Use cero para impedir la recuperación de la posición como una cadena. Si el dispositivo admite pistas, la información de la posición de la cadena se devuelve con el formato TT:MM:SS:FF, donde TT corresponde a pistas, MM y SS corresponden a minutos y segundos, y FF corresponde a fotogramas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un entero correspondiente a la posición actual. Las unidades del valor de posición dependen del formato de hora actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
</dt> <dt>

[**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
</dt> </dl>

 

 





