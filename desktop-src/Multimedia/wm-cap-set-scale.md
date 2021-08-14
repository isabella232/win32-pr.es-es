---
title: WM_CAP_SET_SCALE mensaje (Vfw.h)
description: El mensaje WM CAP SET SCALE habilita o deshabilita \_ el escalado de las imágenes de vídeo en versión \_ \_ preliminar.
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
ms.openlocfilehash: 3293be6917917581957df0f5dae9456274f1d2cc3eeffff5ea971c3596209a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369399"
---
# <a name="wm_cap_set_scale-message"></a>Mensaje \_ WM CAP SET \_ \_ SCALE

El **mensaje WM CAP SET \_ \_ \_ SCALE** habilita o deshabilita el escalado de las imágenes de vídeo en versión preliminar. Si el escalado está habilitado, el fotograma de vídeo capturado se extiende a las dimensiones de la ventana de captura. Puede enviar este mensaje explícitamente o mediante la [**macro capPreviewScale.**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale)


```C++
WM_CAP_SET_SCALE 
wParam = (WPARAM) (BOOL)f; 
lParam = 0L; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

Marca de escalado de vista previa. Especifique **TRUE** para este parámetro para ampliar los fotogramas de vista previa al tamaño de la ventana de captura o **FALSE** para mostrarlos en su tamaño natural.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

## <a name="remarks"></a>Comentarios

El escalado de imágenes de vista previa controla la presentación inmediata de los fotogramas capturados dentro de la ventana de captura. No tiene ningún efecto en el tamaño de los fotogramas guardados en el archivo.

El escalado no tiene ningún efecto al usar la superposición para mostrar vídeo en el búfer de fotogramas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





