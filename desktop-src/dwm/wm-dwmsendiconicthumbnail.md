---
title: Mensaje de WM_DWMSENDICONICTHUMBNAIL (dwmapi. h)
description: Indica a una ventana que proporcione un mapa de bits estático para usarlo como representación en miniatura de la ventana.
ms.assetid: 476c2542-f4d0-4777-93d3-bf50da26d94f
keywords:
- WM_DWMSENDICONICTHUMBNAIL Administrador de ventanas de escritorio de mensaje
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICTHUMBNAIL
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded5b734278973afe35f5ed3d9fbb5b0aec9242b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492658"
---
# <a name="wm_dwmsendiconicthumbnail-message"></a>Mensaje de DWMSENDICONICTHUMBNAIL de WM \_

Indica a una ventana que proporcione un mapa de bits estático para usarlo como representación en miniatura de la ventana.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

El [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de este valor es la coordenada x máxima de la miniatura. [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es la coordenada y máxima. Si una miniatura tiene una dimensión que supera uno o ambos valores, el DWM no acepta la miniatura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

DWM envía este mensaje a una ventana si se cumplen todas las situaciones siguientes:

-   DWM muestra una representación icónica de la ventana.
-   El atributo DWMWA tiene el atributo de [**mapa de \_ \_ \_ bits de iconos**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) en la ventana.
-   La ventana no estableció un mapa de bits almacenado en caché.
-   Hay espacio en la memoria caché para otro mapa de bits.

La ventana que recibe este mensaje debe responder generando un mapa de bits que no sea mayor que el tamaño solicitado en los parámetros del mensaje. A continuación, la ventana llama a la función [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) para reemplazar la miniatura predeterminada. Si la ventana no proporciona un mapa de bits en un período de tiempo determinado, DWM usa su propia representación predeterminada de iconos para la ventana.

La ventana debe pertenecer al proceso de llamada.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo responder al mensaje de **\_ DWMSENDICONICTHUMBNAIL de WM** . En el ejemplo se llama a [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail), con un identificador para un mapa de bits personalizado independiente del dispositivo que se va a usar como representación de Windows.


```C++
        case WM_DWMSENDICONICTHUMBNAIL:
        {    
            // This window is being asked to provide its iconic bitmap. This indicates
            // a thumbnail is being drawn.
            hbm = CreateDIB(HIWORD(lParam), LOWORD(lParam)); 
            if (hbm)
            {
                hr = DwmSetIconicThumbnail(hwnd, hbm, 0);
                DeleteObject(hbm);
            }
        }
        break;
```



Para obtener el ejemplo completo, vea el ejemplo de cómo [personalizar una miniatura de iconos y un mapa de bits de vista previa dinámica](dwm-sample-customizethumbnail.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Dwmapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DwmInvalidateIconicBitmaps**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[**DWMSENDICONICLIVEPREVIEWBITMAP de WM \_**](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 

