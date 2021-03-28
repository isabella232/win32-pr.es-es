---
description: Enviado por la implementación predeterminada del menú contextual para solicitar a LPFNDFMCALLBACK que invoque un comando de menú extendido.
title: Mensaje de DFM_INVOKECOMMANDEX (ShlObj. h)
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
ms.openlocfilehash: dc96e9d0e4c27be8dee3ed7742874de4a3fb97e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540507"
---
# <a name="dfm_invokecommandex-message"></a><span data-ttu-id="94509-103">DFM \_ INVOKECOMMANDEX</span><span class="sxs-lookup"><span data-stu-id="94509-103">DFM\_INVOKECOMMANDEX message</span></span>

<span data-ttu-id="94509-104">Enviado por la implementación predeterminada del menú contextual para solicitar a [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) que invoque un comando de menú extendido.</span><span class="sxs-lookup"><span data-stu-id="94509-104">Sent by the default context menu implementation to request [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) to invoke an extended menu command.</span></span>


```C++
                DFM_INVOKECOMMANDEX
    wParam = (WPARAM)(int) idCmd;           
    lParam = (LPARAM)(DFMICS) PDFMICS;
            
```



## <a name="parameters"></a><span data-ttu-id="94509-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94509-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94509-106">*idCmd* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="94509-106">*idCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94509-107">IDENTIFICADOR de comando del comando de menú seleccionado.</span><span class="sxs-lookup"><span data-stu-id="94509-107">The command ID of the selected menu command.</span></span> <span data-ttu-id="94509-108">Se reconocen las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="94509-108">The following flags are recognized.</span></span>

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span data-ttu-id="94509-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ cmd \_ eliminar**</span><span class="sxs-lookup"><span data-stu-id="94509-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM\_CMD\_DELETE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span data-ttu-id="94509-110"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="94509-110"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM\_CMD\_MOVE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span data-ttu-id="94509-111"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**\_copiar DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="94509-111"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM\_CMD\_COPY**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span data-ttu-id="94509-112"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM \_ vínculo de CMD \_**</span><span class="sxs-lookup"><span data-stu-id="94509-112"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM\_CMD\_LINK**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="94509-113"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**propiedades de DFM \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="94509-113"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="94509-114">Muestra la interfaz de usuario de **propiedades** del elemento en el que se invocó el menú.</span><span class="sxs-lookup"><span data-stu-id="94509-114">Show the **Properties** UI for the item the menu was invoked on.</span></span>

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span data-ttu-id="94509-115"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ cmd \_ NuevaCarpeta**</span><span class="sxs-lookup"><span data-stu-id="94509-115"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM\_CMD\_NEWFOLDER**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span data-ttu-id="94509-116"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM \_ cmd \_ pegar**</span><span class="sxs-lookup"><span data-stu-id="94509-116"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM\_CMD\_PASTE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span data-ttu-id="94509-117"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM \_ cmd \_ VIEWLIST**</span><span class="sxs-lookup"><span data-stu-id="94509-117"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM\_CMD\_VIEWLIST**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span data-ttu-id="94509-118"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM \_ cmd \_ VIEWDETAILS**</span><span class="sxs-lookup"><span data-stu-id="94509-118"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM\_CMD\_VIEWDETAILS**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span data-ttu-id="94509-119"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM \_ cmd \_ PASTELINK**</span><span class="sxs-lookup"><span data-stu-id="94509-119"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM\_CMD\_PASTELINK**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span data-ttu-id="94509-120"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ cmd \_ PASTESPECIAL**</span><span class="sxs-lookup"><span data-stu-id="94509-120"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM\_CMD\_PASTESPECIAL**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span data-ttu-id="94509-121"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ cmd \_ MODALPROP**</span><span class="sxs-lookup"><span data-stu-id="94509-121"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM\_CMD\_MODALPROP**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span data-ttu-id="94509-122"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM \_ cmd \_ Rename**</span><span class="sxs-lookup"><span data-stu-id="94509-122"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM\_CMD\_RENAME**</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="94509-123">*PDFMICS* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="94509-123">*PDFMICS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94509-124">Puntero a una estructura [**DFMICS**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) que contiene argumentos adicionales para el comando de menú seleccionado.</span><span class="sxs-lookup"><span data-stu-id="94509-124">A pointer to a [**DFMICS**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) structure that contains additional arguments to the selected menu command.</span></span> <span data-ttu-id="94509-125">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="94509-125">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94509-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94509-126">Remarks</span></span>

<span data-ttu-id="94509-127">Tras recibir este mensaje, la función debe devolver S \_ false si desea que la implementación predeterminada invoque el controlador predeterminado para el comando.</span><span class="sxs-lookup"><span data-stu-id="94509-127">Upon receipt of this message, your function should return S\_FALSE if you want the default implementation to invoke the default handler for the command.</span></span> <span data-ttu-id="94509-128">Vuelva a \_ Aceptar si el mensaje se ha controlado.</span><span class="sxs-lookup"><span data-stu-id="94509-128">Return S\_OK if the message was handled.</span></span> <span data-ttu-id="94509-129">De lo contrario, devuelve un código de error HRESULT estándar.</span><span class="sxs-lookup"><span data-stu-id="94509-129">Otherwise, return a standard HRESULT error code.</span></span>

<span data-ttu-id="94509-130">Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada, dependiendo de cómo se implemente la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="94509-130">This message is sent to either the callback function or the callback object depending on how the callback is implemented.</span></span> <span data-ttu-id="94509-131">Hay dos API para la construcción de devolución de llamada, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) que toma un puntero a una función de devolución de llamada o [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) que usa un objeto de devolución de llamada que admite [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span><span class="sxs-lookup"><span data-stu-id="94509-131">There are two APIs for callback construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) that takes a pointer to a callback function, or [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) that uses a callback object that supports [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span></span>

<span data-ttu-id="94509-132">Los elementos en los que se invoca el comando se proporcionan en un objeto de datos que se pasa a la función de devolución de llamada o al método [**IContextMenuCB:: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) .</span><span class="sxs-lookup"><span data-stu-id="94509-132">The items on which the command is being invoked are provided in a data object passed to the callback function or to the [**IContextMenuCB::CallBack**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) method.</span></span> <span data-ttu-id="94509-133">Este objeto de datos lo proporciona el origen de datos que implementa la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="94509-133">This data object is provided by the data source that implements the callback.</span></span> <span data-ttu-id="94509-134">Para extraer los elementos del objeto de datos, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span><span class="sxs-lookup"><span data-stu-id="94509-134">To extract the items from the data object, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span></span>

<span data-ttu-id="94509-135">[**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md) es una versión más sencilla de este mensaje que no proporciona tanta información a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="94509-135">[**DFM\_INVOKECOMMAND**](dfm-invokecommand.md) is a simpler version of this message which does not provide as much information to the callback.</span></span> <span data-ttu-id="94509-136">Use **DFM \_ INVOKECOMMAND** si la información adicional proporcionada por **DFM \_ INVOKECOMMANDEX** no es necesaria en su implementación.</span><span class="sxs-lookup"><span data-stu-id="94509-136">Use **DFM\_INVOKECOMMAND** if the additional information provided by **DFM\_INVOKECOMMANDEX** is not needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="94509-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94509-137">Requirements</span></span>



| <span data-ttu-id="94509-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="94509-138">Requirement</span></span> | <span data-ttu-id="94509-139">Value</span><span class="sxs-lookup"><span data-stu-id="94509-139">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="94509-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94509-140">Minimum supported client</span></span><br/> | <span data-ttu-id="94509-141">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="94509-141">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="94509-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94509-142">Minimum supported server</span></span><br/> | <span data-ttu-id="94509-143">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="94509-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="94509-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94509-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="94509-145"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="94509-145"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
