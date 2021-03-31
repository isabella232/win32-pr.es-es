---
title: Mensaje de WM_DWMSENDICONICLIVEPREVIEWBITMAP (dwmapi. h)
description: Indica a una ventana que proporcione un mapa de bits estático para usarlo como vista previa dinámica (también conocida como vista previa de PEEK) de esa ventana.
ms.assetid: 24bf3b42-a850-4aa5-966a-29baab6b4d21
keywords:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP Administrador de ventanas de escritorio de mensaje
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
ms.openlocfilehash: 21f73076ab313da66171bc8265f7f4e7d068f93e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490894"
---
# <a name="wm_dwmsendiconiclivepreviewbitmap-message"></a>Mensaje de DWMSENDICONICLIVEPREVIEWBITMAP de WM \_

Indica a una ventana que proporcione un mapa de bits estático para usarlo como *vista previa dinámica* (también conocida como *vista previa de PEEK*) de esa ventana.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Una *vista previa dinámica* (también conocida como *vista previa PEEK*) de una ventana aparece cuando un usuario mueve el puntero del mouse sobre la miniatura de la ventana en la barra de tareas o le da el foco de miniatura en la ventana Alt + Tab. Esta vista es una vista previa de tamaño completo de la ventana y puede ser una instantánea en directo o una representación de iconos.

Administrador de ventanas de escritorio (DWM) envía este mensaje a una ventana si se cumplen todas las situaciones siguientes:

-   La vista previa dinámica se ha invocado en la ventana de.
-   El atributo DWMWA tiene el atributo de [**mapa de \_ \_ \_ bits de iconos**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) en la ventana.
-   Una representación de iconos es la única que existe para esta ventana.

La ventana que recibe este mensaje debe responder generando un mapa de bits a gran escala. A continuación, la ventana llama a la función [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) para establecer la vista previa dinámica. Si la ventana no establece un mapa de bits en un período de tiempo determinado, DWM usa su propia representación predeterminada de iconos para la ventana.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra una respuesta al mensaje de **\_ DWMSENDICONICLIVEPREVIEWBITMAP de WM** . En el ejemplo se llama a la función [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) con un identificador para un mapa de bits personalizado independiente del dispositivo que se va a usar como representación de la ventana.


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



Para obtener el código completo, vea el ejemplo de cómo [personalizar una miniatura de iconos y un mapa de bits de vista previa dinámica](dwm-sample-customizethumbnail.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Dwmapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DWMSENDICONICTHUMBNAIL de WM \_**](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[**DwmInvalidateIconicBitmaps**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 





