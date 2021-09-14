---
title: TDM_SET_ELEMENT_TEXT mensaje (Commctrl.h)
description: 'TDM_SET_ELEMENT_TEXT mensaje: actualiza un elemento de texto en un cuadro de diálogo de tarea.'
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- TDM_SET_ELEMENT_TEXT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TDM_SET_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d0c8830a6d8a1057ab283a9e096434a6184151
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166129"
---
# <a name="tdm_set_element_text-message"></a>Mensaje DE \_ TEXTO DEL ELEMENTO SET \_ \_ de TDM

Actualiza un elemento de texto en un cuadro de diálogo de tarea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Indica el elemento que se debe actualizar. (Para obtener una ilustración, vea [Acerca de los cuadros de diálogo de tareas).](task-dialogs-overview.md) Este parámetro debe ser uno de los siguientes valores.



| Value                                                                                                                                                                                           | Significado                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**CONTENIDO \_ DE TDE**</dt> </dl>                                         | Contenido.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**INFORMACIÓN EXPANDIDA DE TDE \_ \_**</dt> </dl> | Información expandida.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**PIE DE PÁGINA DE TDE \_**</dt> </dl>                                            | Texto del pie de página.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**INSTRUCCIÓN PRINCIPAL DE TDE \_ \_**</dt> </dl>             | Instrucción principal.<br/>     |



 

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Nuevo texto que se usará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

El tamaño o el diseño del cuadro de diálogo de tarea pueden cambiar para adaptarse al nuevo texto.

## <a name="examples"></a>Ejemplos

El código de ejemplo siguiente muestra cómo establecer el texto del pie de página en el cuadro de diálogo de tarea representado por *hwnd*.


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TEXTO DEL \_ ELEMENTO UPDATE \_ DE TDM \_**](tdm-update-element-text.md)
</dt> </dl>

 

 





