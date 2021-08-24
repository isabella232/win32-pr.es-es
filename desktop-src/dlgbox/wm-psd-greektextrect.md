---
title: WM_PSD_GREEKTEXTRECT mensaje (Commdlg.h)
description: Notifica al procedimiento de enlace de un cuadro de diálogo Configuración de página, PagePaintHook, que el cuadro de diálogo está a punto de dibujar texto griego dentro del rectángulo de margen de la página de ejemplo.
ms.assetid: ad0a200d-5626-4768-b3bd-73d4e3f0d548
keywords:
- WM_PSD_GREEKTEXTRECT cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_PSD_GREEKTEXTRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c30e4873255a59a86da91b3145d0675f6940ce35081273696ce6c68b70a1560
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726055"
---
# <a name="wm_psd_greektextrect-message"></a>Mensaje \_ DE WM PSD \_ GREEKTEXTRECT

Notifica al procedimiento de enlace de un cuadro de diálogo Configuración de página, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), que el cuadro de diálogo está **a** punto de dibujar texto griego dentro del rectángulo de margen de la página de ejemplo.


```C++
#define WM_USER                  0x0400
#define WM_PSD_GREEKTEXTRECT    (WM_USER+4)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del contexto del dispositivo para la página de ejemplo.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que contiene las coordenadas, en píxeles, del rectángulo de texto griego.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el procedimiento de enlace devuelve **TRUE**, el cuadro de diálogo no dibuja la parte del texto griego de la página de ejemplo.

Si el procedimiento de enlace devuelve **FALSE**, el cuadro de diálogo dibuja la parte de texto griego de la página de ejemplo.

## <a name="remarks"></a>Comentarios

El **cuadro de diálogo Configuración** de página incluye una imagen de una página de ejemplo que muestra cómo afectan las selecciones del usuario a la apariencia de la salida impresa. Al llamar a la [**función PageSetupDlg,**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) puede proporcionar un procedimiento de enlace [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar la apariencia de la página de ejemplo. Cada vez que el cuadro de diálogo está a punto de dibujar el contenido de la página de ejemplo, el cuadro de diálogo envía una secuencia de mensajes al procedimiento de enlace.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))
</dt> <dt>

[**WM \_ PSD \_ PAGESETUPDLG**](wm-psd-pagesetupdlg.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

 

