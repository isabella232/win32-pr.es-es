---
description: Muestra una ventana de ayuda que corresponde a la configuración actual del idioma de la interfaz de usuario.
title: MLHtmlHelp función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLHtmlHelp
- MLHtmlHelpA
- MLHtmlHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.assetid: 1108614d-7034-48da-a4a5-544f8d9af3ca
ms.openlocfilehash: a477ef549b3b8437ba891259c7fecea4730f759e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997268"
---
# <a name="mlhtmlhelp-function"></a><span data-ttu-id="3f034-103">MLHtmlHelp función)</span><span class="sxs-lookup"><span data-stu-id="3f034-103">MLHtmlHelp function</span></span>

<span data-ttu-id="3f034-104">\[Esta función está disponible a través de Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3f034-104">\[This function is available through Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="3f034-105">Podría modificarse o no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3f034-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="3f034-106">Muestra una ventana de ayuda que corresponde a la configuración actual del idioma de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="3f034-106">Displays a help window that corresponds to the current UI language setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f034-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f034-107">Syntax</span></span>


```C++
HWND MLHtmlHelp(
  _In_ HWND      hwndCaller,
  _In_ LPCTSTR   pszFile,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData,
  _In_ DWORD     dwCrossCodePage
);
```



## <a name="parameters"></a><span data-ttu-id="3f034-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f034-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f034-109">*hwndCaller* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f034-109">*hwndCaller* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f034-110">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="3f034-110">Type: **HWND**</span></span>

<span data-ttu-id="3f034-111">Identificador de la ventana primaria que llama a esta función.</span><span class="sxs-lookup"><span data-stu-id="3f034-111">A handle to the parent window that calls this function.</span></span>

</dd> <dt>

<span data-ttu-id="3f034-112">*pszFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f034-112">*pszFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f034-113">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="3f034-113">Type: **LPCTSTR**</span></span>

<span data-ttu-id="3f034-114">Un puntero a un búfer que contiene la ruta de acceso completa de un archivo de ayuda compilado (. chm) o un archivo de tema dentro de un archivo de ayuda especificado.</span><span class="sxs-lookup"><span data-stu-id="3f034-114">A pointer to a buffer that contains the fully qualified path of a compiled help (.chm) file, or a topic file within a specified help file.</span></span>

</dd> <dt>

<span data-ttu-id="3f034-115">*uCommand* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f034-115">*uCommand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f034-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3f034-116">Type: **UINT**</span></span>

<span data-ttu-id="3f034-117">Comando que se va a completar.</span><span class="sxs-lookup"><span data-stu-id="3f034-117">The command to complete.</span></span> <span data-ttu-id="3f034-118">Esta función solo admite directamente [el \_ \_ tema de presentación de HH](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) y el [ \_ \_ \_ menú emergente de texto para mostrar HH](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command).</span><span class="sxs-lookup"><span data-stu-id="3f034-118">This function directly supports only [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) and [HH\_DISPLAY\_TEXT\_POPUP](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command).</span></span> <span data-ttu-id="3f034-119">En el caso de cualquier otro comando, la llamada se reenvía sin el valor de *dwCrossCodePage* a [htmlhelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).</span><span class="sxs-lookup"><span data-stu-id="3f034-119">In the case of any other command, the call is forwarded without the *dwCrossCodePage* value to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).</span></span>

</dd> <dt>

<span data-ttu-id="3f034-120">*dwData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f034-120">*dwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f034-121">Tipo: **DWORD \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="3f034-121">Type: **DWORD\_PTR**</span></span>

<span data-ttu-id="3f034-122">Cualquier dato que sea necesario, en función del valor del parámetro *uCommand* .</span><span class="sxs-lookup"><span data-stu-id="3f034-122">Any data that may be required, based on the value of the *uCommand* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3f034-123">*dwCrossCodePage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f034-123">*dwCrossCodePage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f034-124">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3f034-124">Type: **DWORD**</span></span>

<span data-ttu-id="3f034-125">Valor **DWORD** que indica la página de códigos de la configuración actual del idioma de la interfaz de usuario, como CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="3f034-125">The **DWORD** value indicating the code page of the current UI language setting, such as CP\_ACP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f034-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f034-126">Return value</span></span>

<span data-ttu-id="3f034-127">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="3f034-127">Type: **HWND**</span></span>

<span data-ttu-id="3f034-128">En función del *uCommand* especificado y del resultado, **MLHtmlHelp** devuelve uno de los siguientes elementos o ambos:</span><span class="sxs-lookup"><span data-stu-id="3f034-128">Depending on the specified *uCommand* and the result, **MLHtmlHelp** returns one or both of the following:</span></span>

-   <span data-ttu-id="3f034-129">Identificador (HWND) de la ventana de ayuda.</span><span class="sxs-lookup"><span data-stu-id="3f034-129">The handle (hwnd) of the help window.</span></span>
-   <span data-ttu-id="3f034-130">**Null**.</span><span class="sxs-lookup"><span data-stu-id="3f034-130">**NULL**.</span></span> <span data-ttu-id="3f034-131">En algunos casos, **null** indica un error. en otros casos, **null** indica que aún no se ha creado la ventana de ayuda.</span><span class="sxs-lookup"><span data-stu-id="3f034-131">In some cases, **NULL** indicates failure; in other cases, **NULL** indicates that the help window has not yet been created.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f034-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f034-132">Remarks</span></span>

<span data-ttu-id="3f034-133">Si surge un problema con la ruta de acceso del archivo de ayuda para el idioma actual, la llamada se reenvía a [htmlhelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) para el control estándar.</span><span class="sxs-lookup"><span data-stu-id="3f034-133">If a problem arises with the path of the help file for the current language, the call is forwarded to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) for standard handling.</span></span>

<span data-ttu-id="3f034-134">Cuando se cierra la ventana de ayuda, el foco vuelve al propietario a menos que el propietario sea el escritorio.</span><span class="sxs-lookup"><span data-stu-id="3f034-134">When the help window is closed, focus returns to the owner unless the owner is the desktop.</span></span> <span data-ttu-id="3f034-135">Si *hwndCaller* es el escritorio, el sistema operativo determina dónde se devuelve el foco.</span><span class="sxs-lookup"><span data-stu-id="3f034-135">If *hwndCaller* is the desktop, then the operating system determines where focus is returned.</span></span>

<span data-ttu-id="3f034-136">Además, si **MLHtmlHelp** envía mensajes de notificación desde la ventana de ayuda, los mensajes se envían a *hwndCaller* siempre que haya habilitado el seguimiento de [mensajes de notificación](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) en la definición de la ventana de ayuda.</span><span class="sxs-lookup"><span data-stu-id="3f034-136">In addition, if **MLHtmlHelp** sends any notification messages from the help window, the messages are sent to *hwndCaller* as long as you have enabled [notification message](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) tracking in the help window definition.</span></span>

## <a name="examples"></a><span data-ttu-id="3f034-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3f034-137">Examples</span></span>

<span data-ttu-id="3f034-138">En el ejemplo siguiente se llama al comando [HH \_ Display \_ topic](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) para abrir el archivo de ayuda denominado help. chm y mostrar su tema predeterminado en la ventana de ayuda denominada `Mainwin` .</span><span class="sxs-lookup"><span data-stu-id="3f034-138">The following example calls the [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) command to open the help file named Help.chm and display its default topic in the help window named `Mainwin`.</span></span> <span data-ttu-id="3f034-139">Por lo general, la ventana de ayuda especificada en este comando es un [visor de ayuda HTML](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics)estándar.</span><span class="sxs-lookup"><span data-stu-id="3f034-139">Generally, the help window specified in this command is a standard [HTML Help Viewer](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics).</span></span>

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> <span data-ttu-id="3f034-140">Al usar esta función, establezca el tamaño de la pila del archivo ejecutable de hospedaje en al menos 100.000.</span><span class="sxs-lookup"><span data-stu-id="3f034-140">When using this function, set the stack size of the hosting executable to at least 100k.</span></span> <span data-ttu-id="3f034-141">Si el tamaño de pila definido es demasiado pequeño, el subproceso creado para ejecutar la ayuda HTML también se creará con este tamaño de pila y se podría producir un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="3f034-141">If the defined stack size is too small, then the thread created to run HTML Help will also be created with this stack size, and the operation could fail.</span></span> <span data-ttu-id="3f034-142">Opcionalmente, puede quitar/STACK de la línea de comandos de vínculo y también quitar cualquier valor de la pila del archivo DEF del ejecutable (el tamaño de pila predeterminado es de 1 MB en este caso).</span><span class="sxs-lookup"><span data-stu-id="3f034-142">Optionally, you can remove /STACK from the link command line, and also remove any STACK setting in the executable's DEF file (default stack size is 1MB in this case).</span></span> <span data-ttu-id="3f034-143">También puede establecer el tamaño de la pila mediante el comando del compilador/Fnumber (el compilador lo pasará al enlazador como/STACK).</span><span class="sxs-lookup"><span data-stu-id="3f034-143">You can also set the stack size using the /Fnumber compiler command (the compiler will pass this to the linker as /STACK).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3f034-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f034-144">Requirements</span></span>



| <span data-ttu-id="3f034-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f034-145">Requirement</span></span> | <span data-ttu-id="3f034-146">Value</span><span class="sxs-lookup"><span data-stu-id="3f034-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f034-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f034-147">Minimum supported client</span></span><br/> | <span data-ttu-id="3f034-148">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3f034-148">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3f034-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f034-149">Minimum supported server</span></span><br/> | <span data-ttu-id="3f034-150">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3f034-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3f034-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f034-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f034-152"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="3f034-152"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="3f034-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3f034-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f034-154"><dt>Shlwapi.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="3f034-154"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="3f034-155">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="3f034-155">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3f034-156">**MLHtmlHelpW** (Unicode) y **MLHtmlHelpA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3f034-156">**MLHtmlHelpW** (Unicode) and **MLHtmlHelpA** (ANSI)</span></span><br/>                                               |



 

 
