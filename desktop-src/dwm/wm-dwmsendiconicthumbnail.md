---
title: WM_DWMSENDICONICTHUMBNAIL mensaje (Dwmapi.h)
description: Indica a una ventana que proporcione un mapa de bits estático que se usará como representación en miniatura de esa ventana.
ms.assetid: 476c2542-f4d0-4777-93d3-bf50da26d94f
keywords:
- WM_DWMSENDICONICTHUMBNAIL mensaje Administrador de ventanas de escritorio
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
ms.openlocfilehash: 3263f34cd59ba68ee895e5d5c77e297144cbadd6c8d8bbaa49ca6272248c2024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842655"
---
# <a name="wm_dwmsendiconicthumbnail-message"></a>Mensaje \_ DWMSENDICONICTHUMBNAIL de WM

Indica a una ventana que proporcione un mapa de bits estático que se usará como representación en miniatura de esa ventana.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa.

</dd> <dt>

*lParam* 
</dt> <dd>

El [**VALOR HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de este valor es la coordenada X máxima de la miniatura. LOWORD [**es**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) la coordenada Y máxima. Si una miniatura tiene una dimensión que supera uno o ambos valores, dwm no acepta la miniatura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Comentarios

DWM envía este mensaje a una ventana si se cumplen todas las situaciones siguientes:

-   DWM muestra una representación iónicas de la ventana.
-   El [**atributo BITMAP \_ DWMWA HAS \_ ICONIC \_**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) se establece en la ventana.
-   La ventana no estableció un mapa de bits almacenado en caché.
-   Hay espacio en la memoria caché para otro mapa de bits.

La ventana que recibe este mensaje debe responder generando un mapa de bits que no sea mayor que el tamaño solicitado en los parámetros del mensaje. A continuación, la ventana llama a la [**función DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) para invalidar la miniatura predeterminada. Si la ventana no proporciona un mapa de bits en un período de tiempo determinado, DWM usa su propia representación iónicas predeterminada para la ventana.

La ventana debe pertenecer al proceso de llamada.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo responder al **mensaje \_ DWMSENDICONICTHUMBNAIL de WM.** En el ejemplo se llama a [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail), con un identificador para un mapa de bits personalizado independiente del dispositivo que se usará como representación de las ventanas.


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



Para obtener el ejemplo completo, consulte el ejemplo [Personalizar una miniatura izónicas y un mapa](dwm-sample-customizethumbnail.md) de bits de live preview.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                             |
| Header<br/>                   | <dl> <dt>Dwmapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DwmInvalidateIconicBitmaps**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[**WM \_ DWMSENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 

