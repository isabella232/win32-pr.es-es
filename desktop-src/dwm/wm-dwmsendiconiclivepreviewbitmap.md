---
title: WM_DWMSENDICONICLIVEPREVIEWBITMAP mensaje (Dwmapi.h)
description: Indica a una ventana que proporcione un mapa de bits estático para usarlo como una vista previa en directo (también conocida como vista previa de Peek) de esa ventana.
ms.assetid: 24bf3b42-a850-4aa5-966a-29baab6b4d21
keywords:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP mensaje Administrador de ventanas de escritorio
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7742b70afad62a42378e50a06a6e40e503bee72309f5f233f9cf8bf62cf41d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985255"
---
# <a name="wm_dwmsendiconiclivepreviewbitmap-message"></a>Mensaje \_ DWMSENDICONICLIVEPREVIEWBITMAP de WM

Indica a una ventana que proporcione un mapa de bits estático para usarlo como una vista previa en directo *(también* conocida como vista previa *de Peek)* de esa ventana.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Comentarios

Aparece *una* vista previa activa (también conocida como vista previa de *Peek)* de una ventana cuando un usuario mueve el puntero del mouse sobre la miniatura de la ventana en la barra de tareas o proporciona el foco de miniatura en la ventana ALT+TAB. Esta vista es una vista previa de tamaño completo de la ventana y puede ser una instantánea en directo o una representación iztica.

Administrador de ventanas de escritorio (DWM) envía este mensaje a una ventana si se cumplen todas las situaciones siguientes:

-   Se ha invocado la versión preliminar en directo en la ventana.
-   El [**atributo BITMAP \_ DWMWA HAS \_ ICONIC \_**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) se establece en la ventana.
-   Una representación iónicas es la única que existe para esta ventana.

La ventana que recibe este mensaje debe responder generando un mapa de bits a escala completa. A continuación, la ventana llama [**a la función DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) para establecer la vista previa activa. Si la ventana no establece un mapa de bits en un período de tiempo determinado, DWM usa su propia representación iztica predeterminada para la ventana.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra una respuesta al mensaje **\_ DWMSENDICONICLIVEPREVIEWBITMAP de WM.** En el ejemplo se llama a la función [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) con un identificador a un mapa de bits personalizado independiente del dispositivo que se usará como representación de la ventana.


```C++
        case WM_DWMSENDICONICLIVEPREVIEWBITMAP:
        {
            // This window is being asked to provide a bitmap to show in Peek preview.
            // This indicates the thumbnail in the taskbar is being previewed.
            RECT rectWindow = {0, 0, 0, 0};
            if (GetClientRect(hwnd, &rectWindow))
            {
                nWidth = rectWindow.right - rectWindow.left;
                nHeight = rectWindow.bottom - rectWindow.top;
            }

            hbm = CreateDIB(nWidth, nHeight);
            if (hbm)
            {
                hr = DwmSetIconicLivePreviewBitmap(hwnd, hbm, NULL, DWM_SIT_DISPLAYFRAME);
                DeleteObject(hbm);
            }
        }
        break;
```



Para obtener el código completo, consulte el ejemplo Customize an Thumbnail and a Live Preview Bitmap (Personalizar una miniatura [izónicas y un mapa](dwm-sample-customizethumbnail.md) de bits de live preview).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                             |
| Header<br/>                   | <dl> <dt>Dwmapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WM \_ DWMSENDICONICTHUMBNAIL**](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[**DwmInvalidateIconicBitmaps**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 





