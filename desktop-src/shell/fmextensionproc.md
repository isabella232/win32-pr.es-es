---
description: Especifica una función de devolución de llamada definida por la aplicación llamada por el administrador de archivos para comunicarse con una extensión del administrador de archivos.
title: Función de devolución de llamada FMExtensionProc (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMExtensionProc
- FMExtensionProcW
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 6e02d655-f7d8-460a-97d2-5b369493e941
ms.openlocfilehash: 40e18dfe64c6d2b24b982cdf891cbb63b091a7ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997212"
---
# <a name="fmextensionproc-callback-function"></a><span data-ttu-id="040dc-103">Función de devolución de llamada FMExtensionProc</span><span class="sxs-lookup"><span data-stu-id="040dc-103">FMExtensionProc callback function</span></span>

<span data-ttu-id="040dc-104">Especifica una función de devolución de llamada definida por la aplicación llamada por el administrador de archivos para comunicarse con una extensión del administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="040dc-104">Specifies an application-defined callback function called by File Manager to communicate with a File Manager extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="040dc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="040dc-105">Syntax</span></span>


```C++
LONG CALLBACK FMExtensionProc(
   HWND hwnd,
   WORD wMsg,
   LONG lParam
);
```



## <a name="parameters"></a><span data-ttu-id="040dc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="040dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="040dc-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="040dc-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="040dc-108">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="040dc-108">Type: **HWND**</span></span>

<span data-ttu-id="040dc-109">Identificador de ventana para el administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="040dc-109">A window handle to File Manager.</span></span> <span data-ttu-id="040dc-110">Una extensión usa este identificador para especificar la ventana primaria de cualquier cuadro de diálogo o cuadro de mensaje que debe mostrar, y para enviar mensajes de consulta al administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="040dc-110">An extension uses this handle to specify the parent window for any dialog box or message box it must display, and to send query messages to File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="040dc-111">*wMsg*</span><span class="sxs-lookup"><span data-stu-id="040dc-111">*wMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="040dc-112">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="040dc-112">Type: **WORD**</span></span>

<span data-ttu-id="040dc-113">Uno de los siguientes mensajes del administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="040dc-113">One of the following File Manager messages.</span></span>

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span data-ttu-id="040dc-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**de 1 a 99**</span><span class="sxs-lookup"><span data-stu-id="040dc-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1 through 99**</span></span>


</dt> <dd>

<span data-ttu-id="040dc-115">El usuario seleccionó un elemento en el menú proporcionado por la extensión.</span><span class="sxs-lookup"><span data-stu-id="040dc-115">User selected an item from the extension-supplied menu.</span></span> <span data-ttu-id="040dc-116">El valor es el identificador del elemento de menú seleccionado.</span><span class="sxs-lookup"><span data-stu-id="040dc-116">The value is the identifier of the selected menu item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span data-ttu-id="040dc-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="040dc-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT\_HELPMENUITEM**</span></span>


</dt> <dd>

<span data-ttu-id="040dc-118">El usuario presionó F1 al seleccionar un menú de extensión o un elemento de comando de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="040dc-118">User pressed F1 while selecting an extension menu or toolbar command item.</span></span> <span data-ttu-id="040dc-119">Indica que la extensión debe llamar a **WinHelp** adecuadamente para el elemento de comando.</span><span class="sxs-lookup"><span data-stu-id="040dc-119">Indicates that the extension should call **WinHelp** appropriately for the command item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span data-ttu-id="040dc-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT \_ HELPSTRING**</span><span class="sxs-lookup"><span data-stu-id="040dc-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT\_HELPSTRING**</span></span>


</dt> <dd>

<span data-ttu-id="040dc-121">El usuario seleccionó un menú de extensión o un elemento de comando de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="040dc-121">User selected an extension menu or toolbar command item.</span></span> <span data-ttu-id="040dc-122">Indica que la extensión debe proporcionar una cadena de ayuda.</span><span class="sxs-lookup"><span data-stu-id="040dc-122">Indicates that the extension should supply a Help string.</span></span>

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span data-ttu-id="040dc-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT \_ INITMENU**</span><span class="sxs-lookup"><span data-stu-id="040dc-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT\_INITMENU**</span></span>


</dt> <dd>

<span data-ttu-id="040dc-124">El usuario seleccionó el menú de la extensión.</span><span class="sxs-lookup"><span data-stu-id="040dc-124">User selected the extension's menu.</span></span> <span data-ttu-id="040dc-125">La extensión debe inicializar los elementos en el menú.</span><span class="sxs-lookup"><span data-stu-id="040dc-125">The extension should initialize items in the menu.</span></span>

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span data-ttu-id="040dc-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**carga de FMEVENT \_**</span><span class="sxs-lookup"><span data-stu-id="040dc-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT\_LOAD**</span></span>


</dt> <dd>

<span data-ttu-id="040dc-127">El administrador de archivos está cargando el archivo DLL de extensión y solicita al archivo DLL información sobre el menú que suministra el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="040dc-127">File Manager is loading the extension DLL and prompts the DLL for information about the menu that the DLL supplies.</span></span>

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span data-ttu-id="040dc-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT \_ SELCHANGE**</span><span class="sxs-lookup"><span data-stu-id="040dc-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT\_SELCHANGE**</span></span>


</dt> <dd>

<span data-ttu-id="040dc-129">Ha cambiado la selección en la ventana Directorio del **Administrador de archivos** o en la ventana Resultados de la **búsqueda** .</span><span class="sxs-lookup"><span data-stu-id="040dc-129">Selection in the **File Manager** directory window or **Search Results** window has changed.</span></span>

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span data-ttu-id="040dc-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="040dc-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT\_TOOLBARLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="040dc-131">El administrador de archivos está creando la barra de herramientas y solicita al archivo DLL de extensión información sobre los botones que el archivo DLL agrega a la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="040dc-131">File Manager is creating the toolbar and prompts the extension DLL for information about any buttons the DLL adds to the toolbar.</span></span>

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span data-ttu-id="040dc-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**descarga de FMEVENT \_**</span><span class="sxs-lookup"><span data-stu-id="040dc-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT\_UNLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="040dc-133">El administrador de archivos está descargando el archivo DLL de extensión.</span><span class="sxs-lookup"><span data-stu-id="040dc-133">File Manager is unloading the extension DLL.</span></span>

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span data-ttu-id="040dc-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**\_actualización de usuarios de FMEVENT \_**</span><span class="sxs-lookup"><span data-stu-id="040dc-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**FMEVENT\_USER\_REFRESH**</span></span>


</dt> <dd>

<span data-ttu-id="040dc-135">El usuario seleccionó el comando **Actualizar** en el menú **ventana** .</span><span class="sxs-lookup"><span data-stu-id="040dc-135">User selected the **Refresh** command from the **Window** menu.</span></span> <span data-ttu-id="040dc-136">La extensión debe actualizar los elementos en el menú, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="040dc-136">The extension should update items in the menu, if necessary.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="040dc-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="040dc-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="040dc-138">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="040dc-138">Type: **LONG**</span></span>

<span data-ttu-id="040dc-139">Valor específico del mensaje.</span><span class="sxs-lookup"><span data-stu-id="040dc-139">Message-specific value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="040dc-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="040dc-140">Return value</span></span>

<span data-ttu-id="040dc-141">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="040dc-141">Type: **LONG**</span></span>

<span data-ttu-id="040dc-142">Devuelve un valor que depende del mensaje de parámetro *wMsg* .</span><span class="sxs-lookup"><span data-stu-id="040dc-142">Returns a value dependent upon the *wMsg* parameter message.</span></span>

## <a name="requirements"></a><span data-ttu-id="040dc-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="040dc-143">Requirements</span></span>



| <span data-ttu-id="040dc-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="040dc-144">Requirement</span></span> | <span data-ttu-id="040dc-145">Value</span><span class="sxs-lookup"><span data-stu-id="040dc-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="040dc-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="040dc-146">Minimum supported client</span></span><br/> | <span data-ttu-id="040dc-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="040dc-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="040dc-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="040dc-148">Minimum supported server</span></span><br/> | <span data-ttu-id="040dc-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="040dc-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="040dc-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="040dc-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="040dc-151"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="040dc-151"><dt>Wfext.h</dt></span></span> </dl> |
| <span data-ttu-id="040dc-152">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="040dc-152">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="040dc-153">**FMExtensionProcW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="040dc-153">**FMExtensionProcW** (Unicode)</span></span><br/>                                          |



 

 




