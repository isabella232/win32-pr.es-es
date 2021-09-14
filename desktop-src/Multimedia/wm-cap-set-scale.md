---
title: WM_CAP_SET_SCALE mensaje (Vfw.h)
description: El mensaje WM \_ CAP SET SCALE habilita o deshabilita el escalado de las imágenes de vídeo de versión \_ \_ preliminar.
ms.assetid: f15f1d18-2c5a-40c1-baa1-0d18549bee23
keywords:
- WM_CAP_SET_SCALE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCALE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd3bfc5dc463d84c935f994519060c33f89b8c0a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161318"
---
# <a name="wm_cap_set_scale-message"></a>Mensaje \_ WM CAP SET \_ \_ SCALE

El **mensaje WM CAP SET \_ \_ \_ SCALE** habilita o deshabilita el escalado de las imágenes de vídeo de versión preliminar. Si el escalado está habilitado, el fotograma de vídeo capturado se extiende a las dimensiones de la ventana de captura. Puede enviar este mensaje explícitamente o mediante la [**macro capPreviewScale.**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale)


```C++
WM_CAP_SET_SCALE 
wParam = (WPARAM) (BOOL)f; 
lParam = 0L; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

Marca de escalado de vista previa. Especifique **TRUE** para este parámetro a fin de ampliar los fotogramas de vista previa al tamaño de la ventana de captura o **FALSE** para mostrarlos en su tamaño natural.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE en **caso** contrario.

## <a name="remarks"></a>Observaciones

El escalado de imágenes de vista previa controla la presentación inmediata de los fotogramas capturados dentro de la ventana de captura. No tiene ningún efecto en el tamaño de los fotogramas guardados en el archivo.

El escalado no tiene ningún efecto al usar la superposición para mostrar vídeo en el búfer de fotogramas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





