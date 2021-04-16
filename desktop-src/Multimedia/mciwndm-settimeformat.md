---
title: Mensaje de MCIWNDM_SETTIMEFORMAT (VFW. h)
description: El \_ mensaje MCIWNDM SETTIMEFORMAT establece el formato de hora de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSetTimeFormat.
ms.assetid: 7de82094-6d35-44fd-88e7-ebd18a558cfd
keywords:
- Mensaje de MCIWNDM_SETTIMEFORMAT de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533801"
---
# <a name="mciwndm_settimeformat-message"></a>MCIWNDM \_ SETTIMEFORMAT

El mensaje **MCIWNDM \_ SETTIMEFORMAT** establece el formato de hora de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) .


```C++
MCIWNDM_SETTIMEFORMAT 
wParam = 0; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Puntero a un búfer que contiene la cadena terminada en null que indica el formato de hora. Especifique "frames" para establecer el formato de hora en los marcos o "MS" para establecer el formato de hora en milisegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Una aplicación puede especificar formatos de hora que no sean fotogramas o milisegundos, siempre que el dispositivo MCI admita los formatos. Los formatos no continuos, como las pistas y SMPTE, pueden hacer que la barra de seguimiento se comporte de forma errática. Para estos formatos de hora, puede que desee desactivar la barra de herramientas mediante la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) y especificar el estilo de \_ ventana MCIWNDF NOPLAYBAR.

Si desea establecer el formato de hora en fotogramas o milisegundos, también puede usar la macro [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) o [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) . Para obtener una lista de formatos de hora, vea la macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



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

 

 





