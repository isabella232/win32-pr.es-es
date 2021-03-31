---
title: Mensaje de TDM_UPDATE_ELEMENT_TEXT (commctrl. h)
description: Actualiza un elemento de texto en un cuadro de diálogo de tarea.
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- TDM_UPDATE_ELEMENT_TEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_UPDATE_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6dac6787c68d0cbe619bbf28fa1a6383606e99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151141"
---
# <a name="tdm_update_element_text-message"></a>\_Mensaje de \_ texto de elemento de actualización de TDM \_

Actualiza un elemento de texto en un cuadro de diálogo de tarea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Indica el elemento que se va a actualizar. (Para ver una ilustración de los elementos, vea acerca de los [cuadros de diálogo de tareas](task-dialogs-overview.md)). Este parámetro debe ser uno de los siguientes valores:



| Value                                                                                                                                                                                           | Significado                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**contenido de TDE \_**</dt> </dl>                                         | Contenido.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**TDE \_ información expandida \_**</dt> </dl> | Información expandida.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**pie de página de TDE \_**</dt> </dl>                                            | Texto del pie de página.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**\_instrucción principal de TDE \_**</dt> </dl>             | Instrucción principal.<br/>     |



 

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode que contiene el nuevo texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

Para evitar el recorte, el nuevo texto no debe ser mayor que el texto existente. Si se establece el texto en una cadena más corta, no se cambia el tamaño del cuadro de diálogo.

Si el miembro **pszExpandedInformation** de la estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilizada para crear el cuadro de diálogo de tarea era **null** y se envía un mensaje de texto de **\_ \_ elemento \_ de actualización TDM** con \_ información ampliada de TDE, no se producirá \_ nada.

Lo anterior también se aplica al pie de página y al pie de página de TDE \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_texto del \_ elemento de conjunto de TDM \_**](tdm-set-element-text.md)
</dt> </dl>

 

 





