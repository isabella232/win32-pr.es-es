---
title: Mensaje de TB_LOADIMAGES (commctrl. h)
description: Carga las imágenes de botón definidas por el sistema en la lista de imágenes de un control de barra de herramientas.
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- TB_LOADIMAGES controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_LOADIMAGES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0ba6bf75855a0b81ac56438489d7eced3d589
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491981"
---
# <a name="tb_loadimages-message"></a>\_Mensaje LOADIMAGES TB

Carga las imágenes de botón definidas por el sistema en la lista de imágenes de un control de barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de una lista de imágenes de botón definidas por el sistema. Este parámetro se puede establecer en uno de los valores siguientes.



| Value                                                                                                                                                                                | Significado                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <dt>**\_ \_ color grande de hist de IDB \_**</dt> </dl> | Mapas de bits del explorador de Windows de gran tamaño.<br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <dt>**\_ \_ color pequeño de hist de IDB \_**</dt> </dl> | Mapas de bits del explorador de Windows en tamaño pequeño.<br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <dt>**\_ \_ color alto de IDB STD \_**</dt> </dl>    | Mapas de bits estándar de gran tamaño.<br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <dt>**\_ \_ color pequeño de IDB STD \_**</dt> </dl>    | Mapas de bits estándar en tamaño pequeño.<br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <dt>**\_ \_ color grande de la vista IDB \_**</dt> </dl> | Vea los mapas de bits de gran tamaño.<br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <dt>**\_ \_ color pequeño de la vista IDB \_**</dt> </dl> | Vea los mapas de bits en tamaño pequeño.<br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <dt>**HIST de IDB \_ \_ normal**</dt> </dl>                 | Los botones de desplazamiento y los mapas de bits de favoritos del explorador de Windows en estado normal.<br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <dt>**HIST de IDB \_ \_ activo**</dt> </dl>                          | Los botones de desplazamiento y los mapas de bits de favoritos del explorador de Windows en estado activo.<br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <dt>**HIST de IDB \_ \_ deshabilitado**</dt> </dl>           | Los botones de desplazamiento y los mapas de bits de favoritos del explorador de Windows en estado deshabilitado.<br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <dt>**HIST de IDB \_ \_ presionado**</dt> </dl>              | Botones de desplazamiento y favoritos del explorador de Windows en estado presionado.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de instancia. Este parámetro debe establecerse en HINST \_ commctrl.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Recuento de imágenes de la lista de imágenes. Devuelve cero si la barra de herramientas no tiene una lista de imágenes o si la lista de imágenes existente está vacía.

## <a name="remarks"></a>Observaciones

Debe usar los valores de índice de imagen adecuados al preparar las estructuras de [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) antes de enviar el mensaje de [**TB \_ ADDBUTTONS**](tb-addbuttons.md) . Para obtener una lista de valores de índice de imagen para estos mapas de bits predeterminados, vea [valores de índice de imagen de botón estándar](toolbar-standard-button-image-index-values.md)de la barra de herramientas.

## <a name="examples"></a>Ejemplos

En el código de ejemplo siguiente se cargan las imágenes de color pequeño estándar del sistema.


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TB \_ ADDBITMAP**](tb-addbitmap.md)
</dt> </dl>

 

 





