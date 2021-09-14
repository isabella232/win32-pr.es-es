---
title: TB_LOADIMAGES mensaje (Commctrl.h)
description: Carga imágenes de botón definidas por el sistema en la lista de imágenes de un control de barra de herramientas.
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- TB_LOADIMAGES controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166697"
---
# <a name="tb_loadimages-message"></a>Mensaje \_ LOADIMAGES de TB

Carga imágenes de botón definidas por el sistema en la lista de imágenes de un control de barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de una lista de imágenes de botón definidas por el sistema. Este parámetro se puede establecer en uno de los valores siguientes.



| Value                                                                                                                                                                                | Significado                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <dt>**COLOR \_ GRANDE DE IDB HIST \_ \_**</dt> </dl> | Windows Mapas de bits del explorador en gran tamaño.<br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <dt>**COLOR PEQUEÑO \_ DE IDB HIST \_ \_**</dt> </dl> | Windows Mapas de bits del explorador en tamaño pequeño.<br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <dt>**COLOR GRANDE STD de IDB \_ \_ \_**</dt> </dl>    | Mapas de bits estándar de gran tamaño.<br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <dt>**COLOR PEQUEÑO STD de IDB \_ \_ \_**</dt> </dl>    | Mapas de bits estándar en tamaño pequeño.<br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <dt>**VISTA DE IDB \_ \_ COLOR \_ GRANDE**</dt> </dl> | Ver mapas de bits en tamaño grande.<br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <dt>**VISTA DE IDB \_ \_ COLOR \_ PEQUEÑO**</dt> </dl> | Ver mapas de bits en tamaño pequeño.<br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <dt>**IDB \_ HIST \_ NORMAL**</dt> </dl>                 | Windows Botones de viaje del explorador y mapas de bits favoritos en estado normal.<br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <dt>**IDB \_ HIST \_ HOT**</dt> </dl>                          | Windows Botones de viaje del explorador y mapas de bits favoritos en estado de acceso rápido.<br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <dt>**IDB \_ HIST \_ DESHABILITADO**</dt> </dl>           | Windows Los botones de viaje del explorador y los mapas de bits favoritos están deshabilitados.<br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <dt>**IDB \_ HIST \_ PRESSED**</dt> </dl>              | Windows Botones de viaje del explorador y mapas de bits favoritos en estado presionado.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de instancia. Este parámetro debe establecerse en \_ COMMCTRL DE SEST.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Recuento de imágenes de la lista de imágenes. Devuelve cero si la barra de herramientas no tiene ninguna lista de imágenes o si la lista de imágenes existente está vacía.

## <a name="remarks"></a>Observaciones

Debe usar los valores de índice de imagen adecuados al preparar las estructuras [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) antes de enviar el [**mensaje \_ ADDBUTTONS de TB.**](tb-addbuttons.md) Para obtener una lista de valores de índice de imagen para estos mapas de bits preestablecidos, vea Valores de índice de imagen de botón estándar de la barra de [herramientas.](toolbar-standard-button-image-index-values.md)

## <a name="examples"></a>Ejemplos

El código de ejemplo siguiente carga las imágenes de color pequeñas estándar del sistema.


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TB \_ ADDBITMAP**](tb-addbitmap.md)
</dt> </dl>

 

 





