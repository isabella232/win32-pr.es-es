---
title: WM_PSD_PAGESETUPDLG mensaje (Commdlg.h)
description: Notifica a un procedimiento de enlace PagePaintHook que el cuadro de diálogo Configurar página está a punto de dibujar el contenido de la página de ejemplo. El procedimiento de enlace puede usar este mensaje para llevar a cabo tareas de inicialización relacionadas con el dibujo del contenido de la página de ejemplo.
ms.assetid: 0d95240b-7d77-4819-8e5c-cc25cd1b30f2
keywords:
- WM_PSD_PAGESETUPDLG diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_PSD_PAGESETUPDLG
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d775bdeae029ff1657ce33bfb564a651bdee4fbce19ad79431dda2d6036bd0b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787415"
---
# <a name="wm_psd_pagesetupdlg-message"></a>Mensaje \_ \_ PAGESETUPDLG de WM PSD

Notifica a un procedimiento de enlace [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) que el cuadro de diálogo **Configurar** página está a punto de dibujar el contenido de la página de ejemplo. El procedimiento de enlace puede usar este mensaje para llevar a cabo tareas de inicialización relacionadas con el dibujo del contenido de la página de ejemplo.


```C++
#define WM_USER                  0x0400
#define WM_PSD_PAGESETUPDLG     (WM_USER  )
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden bajo especifica un valor que indica el tamaño del papel. Este valor puede ser uno de los **valores de \_ DMPAPER** enumerados en la descripción de la estructura. La palabra de orden superior especifica la orientación del papel o el sobre, y si la impresora es una matriz de puntos o un dispositivo HPPCL (Lenguaje de control de impresoras de HpPCL). Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                             | Significado                                            |
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>0x0001</dt> </dl> | Papel en modo horizontal (matriz de puntos)<br/>    |
| <dl> <dt>0x0003</dt> </dl> | Papel en modo horizontal (HPPCL)<br/>         |
| <dl> <dt>0x0005</dt> </dl> | Papel en modo vertical (matriz de puntos)<br/>     |
| <dl> <dt>0x0007</dt> </dl> | Papel en modo vertical (HPPCL)<br/>          |
| <dl> <dt>0x000b</dt> </dl> | Sobre en modo horizontal (HPPCL)<br/>      |
| <dl> <dt>0x000d</dt> </dl> | Sobre en modo vertical (matriz de puntos)<br/>  |
| <dl> <dt>0x0019</dt> </dl> | Sobre en modo horizontal (matriz de puntos)<br/> |
| <dl> <dt>0x001f</dt> </dl> | Sobre en modo vertical (HPPCL)<br/>       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) que contiene información utilizada para inicializar el cuadro **de diálogo Configurar** página.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el procedimiento de enlace devuelve **TRUE**, el cuadro de diálogo no envía más mensajes y no dibuja en la página de ejemplo hasta la próxima vez que el sistema necesite volver a dibujar la página de ejemplo.

Si el procedimiento de enlace devuelve **FALSE**, el cuadro de diálogo envía los mensajes restantes de la secuencia de dibujo.

## <a name="remarks"></a>Comentarios

El **cuadro de diálogo** Configuración de página incluye una imagen de una página de ejemplo que muestra cómo afectan las selecciones del usuario a la apariencia de la salida impresa. Al llamar a la [**función PageSetupDlg,**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) puede proporcionar un procedimiento de enlace [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar la apariencia de la página de ejemplo. Cada vez que el cuadro de diálogo está a punto de dibujar el contenido de la página de ejemplo, el cuadro de diálogo envía una secuencia de mensajes al procedimiento de enlace.

Los tres primeros mensajes de una secuencia de dibujo **(WM \_ PSD \_ PAGESETUPDLG,** [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)o [**WM \_ PSD \_ MINMARGINRECT)**](wm-psd-minmarginrect.md)proporcionan información que el procedimiento de enlace puede usar para dibujar el contenido de la página de ejemplo. Los mensajes restantes [**(WM \_ PSD \_ MARGINRECT,**](wm-psd-marginrect.md) [**WM \_ PSD \_ GREEKTEXTRECT**](wm-psd-greektextrect.md), [**WM \_ PSD \_ ENVSTAMPRECT**](wm-psd-envstamprect.md), [**WM \_ PSD \_ YAFULLPAGERECT**](wm-psd-yafullpagerect.md)) notifican al procedimiento de enlace que el cuadro de diálogo está a punto de dibujar una parte específica de la página de ejemplo. Esto permite que el procedimiento de enlace dibuje selectivamente partes de la página de ejemplo.

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

[**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[**WM \_ PSD \_ ENVSTAMPRECT**](wm-psd-envstamprect.md)
</dt> <dt>

[**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)
</dt> <dt>

[**WM \_ PSD \_ GREEKTEXTRECT**](wm-psd-greektextrect.md)
</dt> <dt>

[**WM \_ PSD \_ MARGINRECT**](wm-psd-marginrect.md)
</dt> <dt>

[**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)
</dt> <dt>

[**WM \_ PSD \_ YAFULLPAGERECT**](wm-psd-yafullpagerect.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

 

