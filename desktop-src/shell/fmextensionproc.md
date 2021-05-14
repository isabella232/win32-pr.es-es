---
description: Especifica una función de devolución de llamada definida por la aplicación a la que llama el Administrador de archivos para comunicarse con una extensión del Administrador de archivos.
title: Función de devolución de llamada FMExtensionProc (Wfext.h)
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
ms.openlocfilehash: 5e7b1f0142ea77967af15087131d3036aaec505e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842246"
---
# <a name="fmextensionproc-callback-function"></a><span data-ttu-id="e0cf6-103">Función de devolución de llamada FMExtensionProc</span><span class="sxs-lookup"><span data-stu-id="e0cf6-103">FMExtensionProc callback function</span></span>

<span data-ttu-id="e0cf6-104">Especifica una función de devolución de llamada definida por la aplicación a la que llama el Administrador de archivos para comunicarse con una extensión del Administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-104">Specifies an application-defined callback function called by File Manager to communicate with a File Manager extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0cf6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0cf6-105">Syntax</span></span>


```C++
LONG CALLBACK FMExtensionProc(
   HWND hwnd,
   WORD wMsg,
   LONG lParam
);
```



## <a name="parameters"></a><span data-ttu-id="e0cf6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0cf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0cf6-107">*Hwnd*</span><span class="sxs-lookup"><span data-stu-id="e0cf6-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e0cf6-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="e0cf6-108">Type: **HWND**</span></span>

<span data-ttu-id="e0cf6-109">Identificador de ventana para el Administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-109">A window handle to File Manager.</span></span> <span data-ttu-id="e0cf6-110">Una extensión usa este identificador para especificar la ventana primaria de cualquier cuadro de diálogo o cuadro de mensaje que debe mostrar y para enviar mensajes de consulta al Administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-110">An extension uses this handle to specify the parent window for any dialog box or message box it must display, and to send query messages to File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="e0cf6-111">*wMsg*</span><span class="sxs-lookup"><span data-stu-id="e0cf6-111">*wMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="e0cf6-112">Tipo: **WORD**</span><span class="sxs-lookup"><span data-stu-id="e0cf6-112">Type: **WORD**</span></span>

<span data-ttu-id="e0cf6-113">Uno de los siguientes mensajes del Administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-113">One of the following File Manager messages.</span></span>

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span data-ttu-id="e0cf6-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**De 1 a 99**</span><span class="sxs-lookup"><span data-stu-id="e0cf6-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1 through 99**</span></span>


</dt> <dd>

<span data-ttu-id="e0cf6-115">El usuario ha seleccionado un elemento en el menú proporcionado por la extensión.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-115">User selected an item from the extension-supplied menu.</span></span> <span data-ttu-id="e0cf6-116">El valor es el identificador del elemento de menú seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-116">The value is the identifier of the selected menu item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span data-ttu-id="e0cf6-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="e0cf6-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT\_HELPMENUITEM**</span></span>


</dt> <dd>

<span data-ttu-id="e0cf6-118">El usuario presionó F1 al seleccionar un menú de extensión o un elemento de comando de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-118">User pressed F1 while selecting an extension menu or toolbar command item.</span></span> <span data-ttu-id="e0cf6-119">Indica que la extensión debe llamar a **WinHelp correctamente** para el elemento de comando.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-119">Indicates that the extension should call **WinHelp** appropriately for the command item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span data-ttu-id="e0cf6-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT \_ HELPSTRING**</span><span class="sxs-lookup"><span data-stu-id="e0cf6-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT\_HELPSTRING**</span></span>


</dt> <dd>

<span data-ttu-id="e0cf6-121">El usuario ha seleccionado un menú de extensión o un elemento de comando de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-121">User selected an extension menu or toolbar command item.</span></span> <span data-ttu-id="e0cf6-122">Indica que la extensión debe proporcionar una cadena de Ayuda.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-122">Indicates that the extension should supply a Help string.</span></span>

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span data-ttu-id="e0cf6-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT \_ INITMENU**</span><span class="sxs-lookup"><span data-stu-id="e0cf6-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT\_INITMENU**</span></span>


</dt> <dd>

<span data-ttu-id="e0cf6-124">El usuario ha seleccionado el menú de la extensión.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-124">User selected the extension's menu.</span></span> <span data-ttu-id="e0cf6-125">La extensión debe inicializar elementos en el menú.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-125">The extension should initialize items in the menu.</span></span>

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span data-ttu-id="e0cf6-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT \_ LOAD**</span><span class="sxs-lookup"><span data-stu-id="e0cf6-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT\_LOAD**</span></span>


</dt> <dd>

<span data-ttu-id="e0cf6-127">El Administrador de archivos está cargando el archivo DLL de extensión y solicita al archivo DLL información sobre el menú que proporciona el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-127">File Manager is loading the extension DLL and prompts the DLL for information about the menu that the DLL supplies.</span></span>

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span data-ttu-id="e0cf6-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT \_ SELCHANGE**</span><span class="sxs-lookup"><span data-stu-id="e0cf6-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT\_SELCHANGE**</span></span>


</dt> <dd>

<span data-ttu-id="e0cf6-129">La selección en la **ventana de directorio del Administrador** de archivos o en la ventana **Resultados de** la búsqueda ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-129">Selection in the **File Manager** directory window or **Search Results** window has changed.</span></span>

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span data-ttu-id="e0cf6-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="e0cf6-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT\_TOOLBARLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="e0cf6-131">El Administrador de archivos crea la barra de herramientas y solicita al archivo DLL de extensión información sobre los botones que el archivo DLL agrega a la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-131">File Manager is creating the toolbar and prompts the extension DLL for information about any buttons the DLL adds to the toolbar.</span></span>

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span data-ttu-id="e0cf6-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT \_ UNLOAD**</span><span class="sxs-lookup"><span data-stu-id="e0cf6-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT\_UNLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="e0cf6-133">El Administrador de archivos está descargando el archivo DLL de extensión.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-133">File Manager is unloading the extension DLL.</span></span>

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span data-ttu-id="e0cf6-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**ACTUALIZACIÓN DE \_ USUARIO DE \_ FMEVENT**</span><span class="sxs-lookup"><span data-stu-id="e0cf6-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**FMEVENT\_USER\_REFRESH**</span></span>


</dt> <dd>

<span data-ttu-id="e0cf6-135">El usuario **seleccionó el comando** Actualizar en el **menú** Ventana.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-135">User selected the **Refresh** command from the **Window** menu.</span></span> <span data-ttu-id="e0cf6-136">La extensión debe actualizar los elementos del menú, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-136">The extension should update items in the menu, if necessary.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e0cf6-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0cf6-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0cf6-138">Tipo: **LONG**</span><span class="sxs-lookup"><span data-stu-id="e0cf6-138">Type: **LONG**</span></span>

<span data-ttu-id="e0cf6-139">Valor específico del mensaje.</span><span class="sxs-lookup"><span data-stu-id="e0cf6-139">Message-specific value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0cf6-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0cf6-140">Return value</span></span>

<span data-ttu-id="e0cf6-141">Tipo: **LONG**</span><span class="sxs-lookup"><span data-stu-id="e0cf6-141">Type: **LONG**</span></span>

<span data-ttu-id="e0cf6-142">Devuelve un valor que depende del mensaje del parámetro *wMsg.*</span><span class="sxs-lookup"><span data-stu-id="e0cf6-142">Returns a value dependent upon the *wMsg* parameter message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0cf6-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0cf6-143">Requirements</span></span>



| <span data-ttu-id="e0cf6-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0cf6-144">Requirement</span></span> | <span data-ttu-id="e0cf6-145">Value</span><span class="sxs-lookup"><span data-stu-id="e0cf6-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e0cf6-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0cf6-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e0cf6-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e0cf6-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e0cf6-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0cf6-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e0cf6-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e0cf6-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e0cf6-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0cf6-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0cf6-151"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="e0cf6-151"><dt>Wfext.h</dt></span></span> </dl> |
| <span data-ttu-id="e0cf6-152">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="e0cf6-152">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e0cf6-153">**FMExtensionProcW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="e0cf6-153">**FMExtensionProcW** (Unicode)</span></span><br/>                                          |



 

 




