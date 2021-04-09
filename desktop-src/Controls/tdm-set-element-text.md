---
title: Mensaje de TDM_SET_ELEMENT_TEXT (commctrl. h)
description: Actualiza un elemento de texto en un cuadro de diálogo de tarea.
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- TDM_SET_ELEMENT_TEXT controles de mensajes de Windows
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
ms.openlocfilehash: 2229dc269f14c9a3b0765675dcc97dc9776b72c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079709"
---
# <a name="tdm_set_element_text-message"></a>\_Mensaje de \_ texto del elemento de conjunto de TDM \_

Actualiza un elemento de texto en un cuadro de diálogo de tarea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Indica el elemento que se va a actualizar. (Para ver una ilustración, consulte Acerca de los [cuadros de diálogo de tareas](task-dialogs-overview.md)). Este parámetro debe ser uno de los valores siguientes.



| Value                                                                                                                                                                                           | Significado                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**contenido de TDE \_**</dt> </dl>                                         | Contenido.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**TDE \_ información expandida \_**</dt> </dl> | Información expandida.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**pie de página de TDE \_**</dt> </dl>                                            | Texto del pie de página.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**\_instrucción principal de TDE \_**</dt> </dl>             | Instrucción principal.<br/>     |



 

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Nuevo texto que se va a usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

El tamaño o el diseño del cuadro de diálogo de la tarea puede cambiar para dar cabida al nuevo texto.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo establecer el texto del pie de página en el cuadro de diálogo de tarea representado por *hWnd*.


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_texto del \_ elemento de actualización de TDM \_**](tdm-update-element-text.md)
</dt> </dl>

 

 





