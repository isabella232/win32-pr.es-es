---
title: TDM_UPDATE_ELEMENT_TEXT mensaje (Commctrl.h)
description: 'TDM_UPDATE_ELEMENT_TEXT mensaje: actualiza un elemento de texto en un cuadro de diálogo de tarea.'
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- TDM_UPDATE_ELEMENT_TEXT controles de Windows mensaje
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
ms.openlocfilehash: c155b426b92645c0b9cdbabe00c44ffa722b89f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166106"
---
# <a name="tdm_update_element_text-message"></a>Mensaje DE \_ TEXTO DEL ELEMENTO UPDATE \_ \_ de TDM

Actualiza un elemento de texto en un cuadro de diálogo de tarea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Indica el elemento que se debe actualizar. (Para obtener una ilustración de los elementos, vea [Acerca de los cuadros de diálogo de tarea).](task-dialogs-overview.md) Este parámetro debe ser uno de los siguientes valores:



| Value                                                                                                                                                                                           | Significado                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**CONTENIDO \_ DE TDE**</dt> </dl>                                         | Contenido.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**INFORMACIÓN EXPANDIDA DE TDE \_ \_**</dt> </dl> | Información expandida.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**PIE DE PÁGINA DE TDE \_**</dt> </dl>                                            | Texto del pie de página.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**INSTRUCCIÓN PRINCIPAL DE TDE \_ \_**</dt> </dl>             | Instrucción principal.<br/>     |



 

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode que contiene el nuevo texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

Para evitar el recorte, el nuevo texto no debe ser mayor que el texto existente. Establecer el texto en una cadena más corta no hace que el cuadro de diálogo cambie de tamaño.

Si el miembro **pszExpandedInformation** de la estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilizada para crear el cuadro de diálogo de tarea era **NULL** y envía un mensaje **\_ TDM UPDATE \_ ELEMENT \_ TEXT** con TDE \_ EXPANDED INFORMATION, no ocurrirá \_ nada.

Lo anterior también se aplica al pie de página y al pie de página de \_ TDE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TEXTO DEL \_ ELEMENTO SET \_ DE TDM \_**](tdm-set-element-text.md)
</dt> </dl>

 

 





