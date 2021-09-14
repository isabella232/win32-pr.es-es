---
title: ICM_ABOUT mensaje (Vfw.h)
description: El ICM acerca de notifica a un controlador de compresión de vídeo que muestre su cuadro de diálogo Acerca de o consulta a un controlador de compresión de vídeo para determinar si tiene un cuadro \_ de diálogo Acerca de. Puede enviar este mensaje explícitamente o mediante la macro ICAbout.
ms.assetid: 6eca69a3-0463-48e6-befb-5003b7515e7d
keywords:
- ICM_ABOUT mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_ABOUT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e03e88993ba1e345a3ea32a9de7adb2d63abe9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062906"
---
# <a name="icm_about-message"></a>\_ICM Mensaje ABOUT

El **ICM \_ about** notifica a un controlador de compresión de vídeo que muestre su cuadro de diálogo Acerca de o consulta a un controlador de compresión de vídeo para determinar si tiene un cuadro de diálogo Acerca de. Puede enviar este mensaje explícitamente o mediante la macro [**ICAbout.**](/windows/desktop/api/Vfw/nf-vfw-icabout)


```C++
ICM_ABOUT 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Identificador de la ventana primaria del cuadro de diálogo mostrado. También puede determinar si un controlador tiene un cuadro de diálogo Acerca de especificando -1 en este parámetro, como en la macro [**ICQueryAbout.**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) El controlador devuelve ICERR OK si tiene un cuadro de diálogo Acerca de o \_ ICERR \_ UNSUPPORTED en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si el controlador admite este mensaje o ICERR \_ UNSUPPORTED en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





