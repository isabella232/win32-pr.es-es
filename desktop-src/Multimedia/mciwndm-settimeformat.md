---
title: MCIWNDM_SETTIMEFORMAT mensaje (Vfw.h)
description: El mensaje SETTIMEFORMAT de MCIWNDM \_ establece el formato de hora de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSetTimeFormat.
ms.assetid: 7de82094-6d35-44fd-88e7-ebd18a558cfd
keywords:
- MCIWNDM_SETTIMEFORMAT mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcec1f0db5accad93211bf1eb6f1c9297e2b9f33
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370760"
---
# <a name="mciwndm_settimeformat-message"></a>Mensaje SETTIMEFORMAT de MCIWNDM \_

El **mensaje \_ SETTIMEFORMAT de MCIWNDM** establece el formato de hora de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetTimeFormat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)


```C++
MCIWNDM_SETTIMEFORMAT 
wParam = 0; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Puntero a un búfer que contiene la cadena terminada en NULL que indica el formato de hora. Especifique "fotogramas" para establecer el formato de hora en fotogramas o "ms" para establecer el formato de hora en milisegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Una aplicación puede especificar formatos de tiempo distintos de fotogramas o milisegundos, siempre y cuando los formatos sean compatibles con el dispositivo MCI. Los formatos no comunes, como tracks y SMPTE, pueden hacer que la barra de seguimiento se comporte de forma errática. Para estos formatos de tiempo, es posible que quiera desactivar la barra de herramientas mediante la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) y especificando el estilo de ventana MCIWNDF \_ NOPLAYBAR.

Si desea establecer el formato de hora en fotogramas o milisegundos, también puede usar la macro [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) o [**MCIWndUseTime.**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) Para obtener una lista de formatos de hora, vea la macro [**MCIWndGetTimeFormat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> <dt>

[**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> <dt>

[**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
</dt> <dt>

[**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
</dt> <dt>

[**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
</dt> </dl>

 

 





