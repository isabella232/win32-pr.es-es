---
title: Mensaje de WM_PSD_MINMARGINRECT (commdlg. h)
description: Notifica a un procedimiento de enlace PagePaintHook las coordenadas del rectángulo de margen en la página de ejemplo. Un cuadro de diálogo Configurar página envía este mensaje cuando está a punto de dibujar el contenido de la página de ejemplo.
ms.assetid: 14977b52-7a6f-4c55-956a-716398a71613
keywords:
- WM_PSD_MINMARGINRECT cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_PSD_MINMARGINRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ec7271026ba7557fcbe3fe17cd890d62eadbca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534725"
---
# <a name="wm_psd_minmarginrect-message"></a>\_ \_ Mensaje MINMARGINRECT de WM PSD

Notifica a un procedimiento de enlace [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) las coordenadas del rectángulo de margen en la página de ejemplo. Un cuadro de diálogo **Configurar página** envía este mensaje cuando está a punto de dibujar el contenido de la página de ejemplo.


```C++
#define WM_USER                  0x0400
#define WM_PSD_MINMARGINRECT    (WM_USER+2)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del contexto de dispositivo para la página de ejemplo.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contiene las coordenadas, en píxeles, del rectángulo de margen mínimo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el procedimiento de enlace devuelve **true**, el cuadro de diálogo no envía más mensajes y no se dibuja en la página de ejemplo hasta la próxima vez que el sistema necesita volver a dibujar la página de ejemplo.

Si el procedimiento de enlace devuelve **false**, el cuadro de diálogo envía el resto de los mensajes de la secuencia de dibujo.

## <a name="remarks"></a>Observaciones

El cuadro de diálogo **Configurar página** incluye una imagen de una página de ejemplo que muestra cómo afectan las selecciones del usuario a la apariencia de la salida impresa. Cuando llame a la función [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , puede proporcionar un procedimiento de enlace [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar la apariencia de la página de ejemplo. Cada vez que el cuadro de diálogo está a punto de dibujar el contenido de la página de ejemplo, el cuadro de diálogo envía una secuencia de mensajes al procedimiento de enlace.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))
</dt> <dt>

[**\_PAGESETUPDLG de PSD de WM \_**](wm-psd-pagesetupdlg.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Biblioteca de cuadros de diálogo comunes](common-dialog-box-library.md)
</dt> </dl>

 

