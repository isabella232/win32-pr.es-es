---
title: TDM_SET_ELEMENT_TEXT mensaje (Commctrl.h)
description: 'TDM_SET_ELEMENT_TEXT mensaje: actualiza un elemento de texto en un cuadro de diálogo de tarea.'
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- TDM_SET_ELEMENT_TEXT de mensajes controles de Windows
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
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104033"
---
# <a name="tdm_set_element_text-message"></a>Mensaje DE \_ TEXTO DEL ELEMENTO SET \_ \_ de TDM

Actualiza un elemento de texto en un cuadro de diálogo de tarea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Indica el elemento que se debe actualizar. (Para obtener una ilustración, vea [Acerca de los cuadros de diálogo de tareas).](task-dialogs-overview.md) Este parámetro debe ser uno de los siguientes valores.



| Valor                                                                                                                                                                                           | Significado                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**CONTENIDO \_ de TDE**</dt> </dl>                                         | Contenido.<br/>              |
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

## <a name="remarks"></a>Comentarios

El tamaño o el diseño del cuadro de diálogo de tarea pueden cambiar para dar cabida al nuevo texto.

## <a name="examples"></a>Ejemplos

El código de ejemplo siguiente muestra cómo establecer el texto del pie de página en el cuadro de diálogo de tarea representado por *hwnd*.


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows \[ Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TEXTO DEL ELEMENTO UPDATE DE TDM \_ \_ \_**](tdm-update-element-text.md)
</dt> </dl>

 

 





