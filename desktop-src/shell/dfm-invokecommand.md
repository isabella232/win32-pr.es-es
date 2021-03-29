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
# <a name="dfm_invokecommand-message"></a><span data-ttu-id="b6183-103">DFM \_ INVOKECOMMAND</span><span class="sxs-lookup"><span data-stu-id="b6183-103">DFM\_INVOKECOMMAND message</span></span>

<span data-ttu-id="b6183-104">Enviado por la implementación predeterminada del menú contextual para solicitar la función de devolución de llamada que controla el menú ([**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) para invocar un comando de menú.</span><span class="sxs-lookup"><span data-stu-id="b6183-104">Sent by the default context menu implementation to request the callback function that handles the menu ([**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) to invoke a menu command.</span></span>


```C++
DFM_INVOKECOMMAND
    wParam = (WPARAM)(int) id;          
    lParam = (LPARAM)(LPWSTR) args;
            
```



## <a name="parameters"></a><span data-ttu-id="b6183-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6183-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6183-106">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="b6183-106">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6183-107">IDENTIFICADOR de comando del comando de menú seleccionado.</span><span class="sxs-lookup"><span data-stu-id="b6183-107">The command ID of the selected menu command.</span></span> <span data-ttu-id="b6183-108">Se reconocen las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="b6183-108">The following flags are recognized:</span></span>

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span data-ttu-id="b6183-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ cmd \_ eliminar**</span><span class="sxs-lookup"><span data-stu-id="b6183-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM\_CMD\_DELETE**</span></span>


</dt> <dd>

<span data-ttu-id="b6183-110">**Windows Vista y versiones posteriores**.</span><span class="sxs-lookup"><span data-stu-id="b6183-110">**Windows Vista and later**.</span></span> <span data-ttu-id="b6183-111">Elimina el elemento actual.</span><span class="sxs-lookup"><span data-stu-id="b6183-111">Delete the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span data-ttu-id="b6183-112"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="b6183-112"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM\_CMD\_MOVE**</span></span>


</dt> <dd>

<span data-ttu-id="b6183-113">**Windows Vista y versiones posteriores**.</span><span class="sxs-lookup"><span data-stu-id="b6183-113">**Windows Vista and later**.</span></span> <span data-ttu-id="b6183-114">Mueve el elemento actual.</span><span class="sxs-lookup"><span data-stu-id="b6183-114">Move the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span data-ttu-id="b6183-115"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**\_copiar DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="b6183-115"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM\_CMD\_COPY**</span></span>


</dt> <dd>

<span data-ttu-id="b6183-116">**Windows Vista y versiones posteriores**.</span><span class="sxs-lookup"><span data-stu-id="b6183-116">**Windows Vista and later**.</span></span> <span data-ttu-id="b6183-117">Copiar el elemento actual.</span><span class="sxs-lookup"><span data-stu-id="b6183-117">Copy the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span data-ttu-id="b6183-118"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM \_ vínculo de CMD \_**</span><span class="sxs-lookup"><span data-stu-id="b6183-118"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM\_CMD\_LINK**</span></span>


</dt> <dd>

<span data-ttu-id="b6183-119">**Windows Vista y versiones posteriores**.</span><span class="sxs-lookup"><span data-stu-id="b6183-119">**Windows Vista and later**.</span></span> <span data-ttu-id="b6183-120">Cree un vínculo al elemento actual.</span><span class="sxs-lookup"><span data-stu-id="b6183-120">Create a link to the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="b6183-121"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**propiedades de DFM \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="b6183-121"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="b6183-122">Muestra la interfaz de usuario de **propiedades** del elemento en el que se invocó el menú.</span><span class="sxs-lookup"><span data-stu-id="b6183-122">Show the **Properties** UI for the item on which the menu was invoked.</span></span>

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span data-ttu-id="b6183-123"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ cmd \_ NuevaCarpeta**</span><span class="sxs-lookup"><span data-stu-id="b6183-123"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM\_CMD\_NEWFOLDER**</span></span>


</dt> <dd>

<span data-ttu-id="b6183-124">No se admite.</span><span class="sxs-lookup"><span data-stu-id="b6183-124">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span data-ttu-id="b6183-125"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM \_ cmd \_ pegar**</span><span class="sxs-lookup"><span data-stu-id="b6183-125"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM\_CMD\_PASTE**</span></span>


</dt> <dd>

<span data-ttu-id="b6183-126">**Windows Vista y versiones posteriores**.</span><span class="sxs-lookup"><span data-stu-id="b6183-126">**Windows Vista and later**.</span></span> <span data-ttu-id="b6183-127">Pegar un elemento en la ubicación actual.</span><span class="sxs-lookup"><span data-stu-id="b6183-127">Paste an item to the current location.</span></span>

</dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span data-ttu-id="b6183-128"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM \_ cmd \_ VIEWLIST**</span><span class="sxs-lookup"><span data-stu-id="b6183-128"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM\_CMD\_VIEWLIST**</span></span>


</dt> <dd>

<span data-ttu-id="b6183-129">No se admite.</span><span class="sxs-lookup"><span data-stu-id="b6183-129">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span data-ttu-id="b6183-130"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM \_ cmd \_ VIEWDETAILS**</span><span class="sxs-lookup"><span data-stu-id="b6183-130"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM\_CMD\_VIEWDETAILS**</span></span>


</dt> <dd>

<span data-ttu-id="b6183-131">No se admite.</span><span class="sxs-lookup"><span data-stu-id="b6183-131">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span data-ttu-id="b6183-132"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM \_ cmd \_ PASTELINK**</span><span class="sxs-lookup"><span data-stu-id="b6183-132"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM\_CMD\_PASTELINK**</span></span>


</dt> <dd>

<span data-ttu-id="b6183-133">**Windows Vista y versiones posteriores**.</span><span class="sxs-lookup"><span data-stu-id="b6183-133">**Windows Vista and later**.</span></span> <span data-ttu-id="b6183-134">Pegar un vínculo en la ubicación actual.</span><span class="sxs-lookup"><span data-stu-id="b6183-134">Paste a link at the current location.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span data-ttu-id="b6183-135"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ cmd \_ PASTESPECIAL**</span><span class="sxs-lookup"><span data-stu-id="b6183-135"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM\_CMD\_PASTESPECIAL**</span></span>


</dt> <dd>

<span data-ttu-id="b6183-136">No se admite.</span><span class="sxs-lookup"><span data-stu-id="b6183-136">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span data-ttu-id="b6183-137"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ cmd \_ MODALPROP**</span><span class="sxs-lookup"><span data-stu-id="b6183-137"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM\_CMD\_MODALPROP**</span></span>


</dt> <dd>

<span data-ttu-id="b6183-138">No se admite.</span><span class="sxs-lookup"><span data-stu-id="b6183-138">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span data-ttu-id="b6183-139"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM \_ cmd \_ Rename**</span><span class="sxs-lookup"><span data-stu-id="b6183-139"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM\_CMD\_RENAME**</span></span>


</dt> <dd>

<span data-ttu-id="b6183-140">**Windows Vista y versiones posteriores**.</span><span class="sxs-lookup"><span data-stu-id="b6183-140">**Windows Vista and later**.</span></span> <span data-ttu-id="b6183-141">Cambiar el nombre del elemento actual.</span><span class="sxs-lookup"><span data-stu-id="b6183-141">Rename the current item.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b6183-142">*argumentos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b6183-142">*args* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6183-143">Un puntero a una cadena terminada en null que contiene argumentos adicionales para el comando de menú seleccionado.</span><span class="sxs-lookup"><span data-stu-id="b6183-143">A pointer to a null-terminated string that contains additional arguments to the selected menu command.</span></span> <span data-ttu-id="b6183-144">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b6183-144">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6183-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6183-145">Return value</span></span>

<span data-ttu-id="b6183-146">El controlador de este mensaje debe devolver S \_ false si desea que la implementación predeterminada invoque el controlador predeterminado para el comando.</span><span class="sxs-lookup"><span data-stu-id="b6183-146">The handler for this message needs to return S\_FALSE if you want the default implementation to invoke the default handler for the command.</span></span> <span data-ttu-id="b6183-147">Vuelva a \_ Aceptar si el mensaje se ha controlado.</span><span class="sxs-lookup"><span data-stu-id="b6183-147">Return S\_OK if the message was handled.</span></span> <span data-ttu-id="b6183-148">De lo contrario, devuelve un código de error HRESULT estándar.</span><span class="sxs-lookup"><span data-stu-id="b6183-148">Otherwise, return a standard HRESULT error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6183-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6183-149">Remarks</span></span>

<span data-ttu-id="b6183-150">Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada, dependiendo de cómo se implemente la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b6183-150">This message is sent to either the callback function or the callback object depending on how the callback is implemented.</span></span> <span data-ttu-id="b6183-151">Hay dos API para la construcción de devolución de llamada, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) que toma un puntero a una función de devolución de llamada o [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) que usa un objeto de devolución de llamada que admite [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span><span class="sxs-lookup"><span data-stu-id="b6183-151">There are two APIs for callback construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) that takes a pointer to a callback function, or [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) that uses a callback object that supports [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span></span>

<span data-ttu-id="b6183-152">Los elementos en los que se invoca el comando se proporcionan en un objeto de datos que se pasa a la función de devolución de llamada o al método [**IContextMenuCB:: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) .</span><span class="sxs-lookup"><span data-stu-id="b6183-152">The items on which the command is being invoked are provided in a data object passed to the callback function or to the [**IContextMenuCB::CallBack**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) method.</span></span> <span data-ttu-id="b6183-153">Este objeto de datos lo proporciona el origen de datos que implementa la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b6183-153">This data object is provided by the data source that implements the callback.</span></span> <span data-ttu-id="b6183-154">Para extraer los elementos del objeto de datos, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span><span class="sxs-lookup"><span data-stu-id="b6183-154">To extract the items from the data object, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span></span>

<span data-ttu-id="b6183-155">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) es una versión extendida de este mensaje y proporciona más información a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b6183-155">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="b6183-156">Use **DFM \_ INVOKECOMMANDEX** si necesita la información adicional proporcionada por esa interfaz en su implementación de.</span><span class="sxs-lookup"><span data-stu-id="b6183-156">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6183-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6183-157">Requirements</span></span>



| <span data-ttu-id="b6183-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6183-158">Requirement</span></span> | <span data-ttu-id="b6183-159">Value</span><span class="sxs-lookup"><span data-stu-id="b6183-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b6183-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6183-160">Minimum supported client</span></span><br/> | <span data-ttu-id="b6183-161">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b6183-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b6183-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6183-162">Minimum supported server</span></span><br/> | <span data-ttu-id="b6183-163">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b6183-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b6183-164">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6183-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6183-165"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6183-165"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
