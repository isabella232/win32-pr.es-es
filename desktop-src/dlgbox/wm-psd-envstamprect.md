---
title: WM_PSD_ENVSTAMPRECT mensaje (Commdlg.h)
description: Notifica al procedimiento de enlace de un cuadro de diálogo De instalación de página, PagePaintHook, que el cuadro de diálogo está a punto de dibujar el rectángulo de marca de sobre de la página de ejemplo.
ms.assetid: f193baa0-a084-416e-90c9-9c838758a3d3
keywords:
- WM_PSD_ENVSTAMPRECT de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_PSD_ENVSTAMPRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bf846779f2fba5c2b2ac85d806c794d3e88aa6dcac0ce906ad82332e2ca2bee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720712"
---
# <a name="wm_psd_envstamprect-message"></a>Mensaje \_ WM PSD \_ ENVSTAMPRECT

Notifica al procedimiento de  enlace de un cuadro de diálogo Configuración de página, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), que el cuadro de diálogo está a punto de dibujar el rectángulo de marca de sobre de la página de ejemplo.


```C++
#define WM_USER                  0x0400
#define WM_PSD_ENVSTAMPRECT     (WM_USER+5)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del contexto del dispositivo para la página de ejemplo.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que contiene las coordenadas, en píxeles, del rectángulo de marca de sobre.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el procedimiento de enlace devuelve **TRUE**, el cuadro de diálogo no dibuja la parte de la marca de sobre de la página de ejemplo.

Si el procedimiento de enlace devuelve **FALSE**, el cuadro de diálogo dibuja la parte de la marca de sobre de la página de ejemplo.

## <a name="remarks"></a>Comentarios

El **cuadro de diálogo Configuración** de página incluye una imagen de una página de ejemplo que muestra cómo afectan las selecciones del usuario a la apariencia de la salida impresa. Al llamar a la [**función PageSetupDlg,**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) puede proporcionar un procedimiento de enlace [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar la apariencia de la página de ejemplo. Cada vez que el cuadro de diálogo está a punto de dibujar el contenido de la página de ejemplo, el cuadro de diálogo envía una secuencia de mensajes al procedimiento de enlace.

Un procedimiento de enlace recibe este mensaje solo si el tipo de papel seleccionado es un sobre.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

