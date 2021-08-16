---
title: WM_PSD_YAFULLPAGERECT mensaje (Commdlg.h)
description: Notifica al procedimiento de enlace de un cuadro de diálogo Configurar página, PagePaintHook, que el cuadro de diálogo está a punto de dibujar la parte de la dirección de devolución de una página de ejemplo de sobre.
ms.assetid: 1f6aea69-a1bd-41ea-b508-44b4f5c38757
keywords:
- WM_PSD_YAFULLPAGERECT cuadros de diálogo del mensaje
topic_type:
- apiref
api_name:
- WM_PSD_YAFULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62cfbd187cb3db5a27579b428c352be1da1a4bdf91f3336ed41511fe59d75d23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787365"
---
# <a name="wm_psd_yafullpagerect-message"></a>Mensaje \_ YAFULLPAGERECT de WM PSD \_

Notifica al procedimiento de  enlace de un cuadro de diálogo Configurar página, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), que el cuadro de diálogo está a punto de dibujar la parte de la dirección de devolución de una página de ejemplo de sobre.


```C++
#define WM_USER                  0x0400
#define WM_PSD_YAFULLPAGERECT   (WM_USER+6)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del contexto del dispositivo para la página de ejemplo.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**RECT**](/previous-versions//dd162897(v=vs.85)) que contiene las coordenadas, en píxeles, de la página de ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el procedimiento de enlace devuelve **TRUE**, el cuadro de diálogo no dibuja la parte de la dirección de retorno de una página de ejemplo de sobre.

Si el procedimiento de enlace devuelve **FALSE**, el cuadro de diálogo dibuja la parte de la dirección de devolución de una página de ejemplo de sobre.

Si el tipo de papel no es un sobre, el valor devuelto no tiene ningún efecto.

## <a name="remarks"></a>Comentarios

El **cuadro de diálogo** Configuración de página incluye una imagen de una página de ejemplo que muestra cómo afectan las selecciones del usuario a la apariencia de la salida impresa. Al llamar a la [**función PageSetupDlg,**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) puede proporcionar un procedimiento de enlace [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar la apariencia de la página de ejemplo. Cada vez que el cuadro de diálogo está a punto de dibujar el contenido de la página de ejemplo, el cuadro de diálogo envía una secuencia de mensajes al procedimiento de enlace.

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

[**PÁGINA \_ DE PSD \_ DE WMSETUPDLG**](wm-psd-pagesetupdlg.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

 

