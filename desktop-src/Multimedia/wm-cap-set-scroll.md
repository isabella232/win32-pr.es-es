---
title: Mensaje de WM_CAP_SET_SCROLL (VFW. h)
description: El \_ \_ mensaje de desplazamiento del conjunto de Cap de WM \_ define la parte del fotograma de vídeo que se va a mostrar en la ventana de captura.
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- Mensaje de WM_CAP_SET_SCROLL de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492946"
---
# <a name="wm_cap_set_scroll-message"></a>\_Mensaje de \_ desplazamiento de conjunto de Cap de WM \_

El mensaje de desplazamiento del conjunto de Cap de WM define la parte del fotograma de vídeo que se va a mostrar en la ventana de captura. **\_ \_ \_** Este mensaje establece la esquina superior izquierda del área de cliente de la ventana de captura en las coordenadas de un píxel especificado dentro del fotograma de vídeo. Puede enviar este mensaje explícitamente o mediante la macro [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) .


```C++
WM_CAP_SET_SCROLL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPPOINT) (lpP); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*lpP*
</dt> <dd>

Dirección que va a contener la posición de desplazamiento deseada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

La posición de desplazamiento afecta a la imagen en los modos de vista previa y de superposición.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





