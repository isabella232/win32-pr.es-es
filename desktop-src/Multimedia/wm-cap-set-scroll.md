---
title: WM_CAP_SET_SCROLL mensaje (Vfw.h)
description: El mensaje \_ WM CAP SET SCROLL define la parte del fotograma de vídeo que se mostrará en la ventana \_ de \_ captura.
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- WM_CAP_SET_SCROLL mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCROLL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812b76bdcad166b9f766957032f232293d4083c0
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371528"
---
# <a name="wm_cap_set_scroll-message"></a>Mensaje \_ WM CAP SET \_ \_ SCROLL

El **mensaje WM CAP SET \_ \_ \_ SCROLL** define la parte del fotograma de vídeo que se mostrará en la ventana de captura. Este mensaje establece la esquina superior izquierda del área cliente de la ventana de captura en las coordenadas de un píxel especificado dentro del marco de vídeo. Puede enviar este mensaje explícitamente o mediante la macro [**capSetScrollPos.**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos)


```C++
WM_CAP_SET_SCROLL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPPOINT) (lpP); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*Lpp*
</dt> <dd>

Dirección que contiene la posición de desplazamiento deseada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

## <a name="remarks"></a>Observaciones

La posición de desplazamiento afecta a la imagen en los modos de vista previa y superposición.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





