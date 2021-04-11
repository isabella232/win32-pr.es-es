---
title: Mensaje de WM_CAP_SET_SCALE (VFW. h)
description: El \_ \_ \_ mensaje de escala del límite de Cap de WM habilita o deshabilita el escalado de las imágenes de vídeo de vista previa.
ms.assetid: f15f1d18-2c5a-40c1-baa1-0d18549bee23
keywords:
- Mensaje de WM_CAP_SET_SCALE de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151096"
---
# <a name="wm_cap_set_scale-message"></a>\_Mensaje de \_ escala de conjunto de Cap de WM \_

El mensaje de **\_ \_ \_ escala del límite de Cap de WM** habilita o deshabilita el escalado de las imágenes de vídeo de vista previa. Si el escalado está habilitado, el fotograma de vídeo capturado se ajusta a las dimensiones de la ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) .


```C++
WM_CAP_SET_SCALE 
wParam = (WPARAM) (BOOL)f; 
lParam = 0L; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="f"></span><span id="F"></span>*formato*
</dt> <dd>

Marca de escala de vista previa. Especifique **true** para que este parámetro Estire los fotogramas de vista previa hasta el tamaño de la ventana de captura o **false** para mostrarlos en su tamaño natural.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Escalar imágenes de vista previa controla la presentación inmediata de los fotogramas capturados en la ventana de captura. No tiene ningún efecto en el tamaño de los fotogramas guardados en el archivo.

El escalado no tiene ningún efecto cuando se usa la superposición para mostrar el vídeo en el búfer de fotogramas.

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

 

 





