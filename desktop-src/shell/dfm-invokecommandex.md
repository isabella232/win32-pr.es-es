---
description: Enviado por la implementación predeterminada del menú contextual para solicitar LPFNDFMCALLBACK para invocar un comando de menú extendido.
title: DFM_INVOKECOMMANDEX mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6ef885e5-2ddd-4a1b-9f8e-016a74e292b1
api_name:
- DFM_INVOKECOMMANDEX
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b8a7fd63aa4269ee265a4ae147c99fe394e8aad725f7134f8d62daf8ee9984b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943175"
---
# <a name="dfm_invokecommandex-message"></a>Mensaje \_ INVOKECOMMANDEX de DFM

Enviado por la implementación predeterminada del menú contextual para solicitar [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) para invocar un comando de menú extendido.


```C++
                DFM_INVOKECOMMANDEX
    wParam = (WPARAM)(int) idCmd;           
    lParam = (LPARAM)(DFMICS) PDFMICS;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*idCmd* \[ en\]
</dt> <dd>

Identificador de comando del comando de menú seleccionado. Se reconocen las marcas siguientes.

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**ELIMINACIÓN \_ DE CMD DE DFM \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**MOVIMIENTO DE CMD DE DFM \_ \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**COPIA DE \_ CMD DE DFM \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**VÍNCULO DE \_ CMD DE DFM \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**PROPIEDADES DE CMD DE DFM \_ \_**


</dt> <dd>

Mostrar la **interfaz de** usuario propiedades del elemento en el que se invocó el menú.

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ CMD \_ NEWFOLDER**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**PEGAR CMD DE DFM \_ \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**LISTA DE VISTAS \_ DE CMD DE DFM \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**VISTA \_ DE CMD DE DFMDETAILS \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**CMD \_ PASTELINK de DFM \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**CMD \_ PASTESPECIAL de DFM \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ CMD \_ MODALPROP**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**CAMBIO DE NOMBRE DE CMD DE DFM \_ \_**


</dt> <dd></dd> </dl> </dd> <dt>

*PDFMICS* \[ En\]
</dt> <dd>

Puntero a una [**estructura DFMICS**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) que contiene argumentos adicionales para el comando de menú seleccionado. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Tras la recepción de este mensaje, la función debe devolver S FALSE si desea que la implementación predeterminada invoque el \_ controlador predeterminado para el comando. Devuelve S \_ OK si se controló el mensaje. De lo contrario, devuelva un código de error HRESULT estándar.

Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada en función de cómo se implemente la devolución de llamada. Hay dos API para la construcción de devolución de llamada, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) que toma un puntero a una función de devolución de llamada o [**SHCreateDefaultContextMenu que**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) usa un objeto de devolución de llamada que admite [**IContextMenuCB.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)

Los elementos en los que se invoca el comando se proporcionan en un objeto de datos pasado a la función de devolución de llamada o al método [**IContextMenuCB::CallBack.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) El origen de datos que implementa la devolución de llamada proporciona este objeto de datos. Para extraer los elementos del objeto de datos, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).

[**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md) es una versión más sencilla de este mensaje que no proporciona tanta información a la devolución de llamada. Use **DFM \_ INVOKECOMMAND si** la información adicional proporcionada por **DFM \_ INVOKECOMMANDEX** no es necesaria en la implementación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
