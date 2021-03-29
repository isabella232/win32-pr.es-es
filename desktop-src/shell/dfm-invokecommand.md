---
description: Enviado por la implementación predeterminada del menú contextual para solicitar la función de devolución de llamada que controla el menú (LPFNDFMCALLBACK) para invocar un comando de menú.
title: Mensaje de DFM_INVOKECOMMAND (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bd3200a6-b9e7-414c-9a01-c432cb306dba
api_name:
- DFM_INVOKECOMMAND
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 168b25833deb6bde2424ea4552f4600b83bc9679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984306"
---
# <a name="dfm_invokecommand-message"></a>DFM \_ INVOKECOMMAND

Enviado por la implementación predeterminada del menú contextual para solicitar la función de devolución de llamada que controla el menú ([**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) para invocar un comando de menú.


```C++
DFM_INVOKECOMMAND
    wParam = (WPARAM)(int) id;          
    lParam = (LPARAM)(LPWSTR) args;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ID.* \[ en\]
</dt> <dd>

IDENTIFICADOR de comando del comando de menú seleccionado. Se reconocen las marcas siguientes:

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ cmd \_ eliminar**


</dt> <dd>

**Windows Vista y versiones posteriores**. Elimina el elemento actual.

</dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM \_ cmd \_**


</dt> <dd>

**Windows Vista y versiones posteriores**. Mueve el elemento actual.

</dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**\_copiar DFM cmd \_**


</dt> <dd>

**Windows Vista y versiones posteriores**. Copiar el elemento actual.

</dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM \_ vínculo de CMD \_**


</dt> <dd>

**Windows Vista y versiones posteriores**. Cree un vínculo al elemento actual.

</dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**propiedades de DFM \_ cmd \_**


</dt> <dd>

Muestra la interfaz de usuario de **propiedades** del elemento en el que se invocó el menú.

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ cmd \_ NuevaCarpeta**


</dt> <dd>

No se admite.

</dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM \_ cmd \_ pegar**


</dt> <dd>

**Windows Vista y versiones posteriores**. Pegar un elemento en la ubicación actual.

</dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM \_ cmd \_ VIEWLIST**


</dt> <dd>

No se admite.

</dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM \_ cmd \_ VIEWDETAILS**


</dt> <dd>

No se admite.

</dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM \_ cmd \_ PASTELINK**


</dt> <dd>

**Windows Vista y versiones posteriores**. Pegar un vínculo en la ubicación actual.

</dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ cmd \_ PASTESPECIAL**


</dt> <dd>

No se admite.

</dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ cmd \_ MODALPROP**


</dt> <dd>

No se admite.

</dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM \_ cmd \_ Rename**


</dt> <dd>

**Windows Vista y versiones posteriores**. Cambiar el nombre del elemento actual.

</dd> </dl> </dd> <dt>

*argumentos* \[ de\]
</dt> <dd>

Un puntero a una cadena terminada en null que contiene argumentos adicionales para el comando de menú seleccionado. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El controlador de este mensaje debe devolver S \_ false si desea que la implementación predeterminada invoque el controlador predeterminado para el comando. Vuelva a \_ Aceptar si el mensaje se ha controlado. De lo contrario, devuelve un código de error HRESULT estándar.

## <a name="remarks"></a>Observaciones

Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada, dependiendo de cómo se implemente la devolución de llamada. Hay dos API para la construcción de devolución de llamada, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) que toma un puntero a una función de devolución de llamada o [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) que usa un objeto de devolución de llamada que admite [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).

Los elementos en los que se invoca el comando se proporcionan en un objeto de datos que se pasa a la función de devolución de llamada o al método [**IContextMenuCB:: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) . Este objeto de datos lo proporciona el origen de datos que implementa la devolución de llamada. Para extraer los elementos del objeto de datos, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) es una versión extendida de este mensaje y proporciona más información a la devolución de llamada. Use **DFM \_ INVOKECOMMANDEX** si necesita la información adicional proporcionada por esa interfaz en su implementación de.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
