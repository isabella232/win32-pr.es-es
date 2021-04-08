---
title: Mensaje de ICM_ABOUT (VFW. h)
description: El \_ mensaje acerca de ICM informa a un controlador de compresión de vídeo para que muestre su cuadro de diálogo acerca de o consulta un controlador de compresión de vídeo para determinar si tiene el cuadro de diálogo acerca de. Puede enviar este mensaje explícitamente o mediante la macro ICAbout.
ms.assetid: 6eca69a3-0463-48e6-befb-5003b7515e7d
keywords:
- Mensaje de ICM_ABOUT de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078843"
---
# <a name="icm_about-message"></a>\_Mensaje acerca de ICM

El **mensaje \_ acerca de ICM** informa a un controlador de compresión de vídeo para que muestre su cuadro de diálogo acerca de o consulta un controlador de compresión de vídeo para determinar si tiene el cuadro de diálogo acerca de. Puede enviar este mensaje explícitamente o mediante la macro [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) .


```C++
ICM_ABOUT 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*identificador*
</dt> <dd>

Identificador de la ventana primaria del cuadro de diálogo que se muestra. También puede determinar si un controlador tiene un cuadro de diálogo acerca de especificando-1 en este parámetro, como en la macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) . El controlador devuelve ICERR \_ OK si tiene un cuadro de diálogo about o ICERR \_ no admitido de otro modo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si el controlador admite este mensaje o ICERR \_ no se admite en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





