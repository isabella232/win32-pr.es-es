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
ms.openlocfilehash: 352d65c2ad8e80622f7ff50cca0a8f7d6e523d53ae002a2325327a634b97c931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134989"
---
# <a name="wm_cap_set_scroll-message"></a>Mensaje DE DESPLAZAMIENTO de WM \_ CAP \_ SET \_

El **mensaje WM CAP SET \_ \_ \_ SCROLL** define la parte del fotograma de vídeo que se mostrará en la ventana de captura. Este mensaje establece la esquina superior izquierda del área cliente de la ventana de captura en las coordenadas de un píxel especificado dentro del fotograma de vídeo. Puede enviar este mensaje explícitamente o mediante la macro [**capSetScrollPos.**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos)


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

## <a name="remarks"></a>Comentarios

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

 

 





