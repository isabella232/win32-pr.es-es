---
description: Muestra una ventana de ayuda que corresponde a la configuración actual del idioma de la interfaz de usuario.
title: Función MLHtmlHelp
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
ms.openlocfilehash: 38d331d57b9484ab6d7a505d929508f30d510ad8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841216"
---
# <a name="mlhtmlhelp-function"></a><span data-ttu-id="c8cf0-103">Función MLHtmlHelp</span><span class="sxs-lookup"><span data-stu-id="c8cf0-103">MLHtmlHelp function</span></span>

<span data-ttu-id="c8cf0-104">\[Esta función está disponible a través de Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c8cf0-104">\[This function is available through Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c8cf0-105">Podría modificarse o no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c8cf0-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="c8cf0-106">Muestra una ventana de ayuda que corresponde a la configuración actual del idioma de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c8cf0-106">Displays a help window that corresponds to the current UI language setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8cf0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8cf0-107">Syntax</span></span>


```C++
HWND MLHtmlHelp(
  _In_ HWND      hwndCaller,
  _In_ LPCTSTR   pszFile,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData,
  _In_ DWORD     dwCrossCodePage
);
```



## <a name="parameters"></a><span data-ttu-id="c8cf0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8cf0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8cf0-109">*hwndCaller* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c8cf0-109">*hwndCaller* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8cf0-110">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="c8cf0-110">Type: **HWND**</span></span>

<span data-ttu-id="c8cf0-111">Identificador de la ventana primaria que llama a esta función.</span><span class="sxs-lookup"><span data-stu-id="c8cf0-111">A handle to the parent window that calls this function.</span></span>

</dd> <dt>

<span data-ttu-id="c8cf0-112">*pszFile* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c8cf0-112">*pszFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8cf0-113">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="c8cf0-113">Type: **LPCTSTR**</span></span>

<span data-ttu-id="c8cf0-114">Puntero a un búfer que contiene la ruta de acceso completa de un archivo de ayuda compilado (.chm) o un archivo de tema dentro de un archivo de ayuda especificado.</span><span class="sxs-lookup"><span data-stu-id="c8cf0-114">A pointer to a buffer that contains the fully qualified path of a compiled help (.chm) file, or a topic file within a specified help file.</span></span>

</dd> <dt>

<span data-ttu-id="c8cf0-115">*uCommand* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c8cf0-115">*uCommand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8cf0-116">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="c8cf0-116">Type: **UINT**</span></span>

<span data-ttu-id="c8cf0-117">Comando que se completará.</span><span class="sxs-lookup"><span data-stu-id="c8cf0-117">The command to complete.</span></span> <span data-ttu-id="c8cf0-118">Esta función solo admite directamente [HH \_ DISPLAY \_ TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) y [HH DISPLAY TEXT \_ \_ \_ POPUP](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command).</span><span class="sxs-lookup"><span data-stu-id="c8cf0-118">This function directly supports only [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) and [HH\_DISPLAY\_TEXT\_POPUP](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command).</span></span> <span data-ttu-id="c8cf0-119">En el caso de cualquier otro comando, la llamada se reenvía sin el valor *dwCrossCodePage* a [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).</span><span class="sxs-lookup"><span data-stu-id="c8cf0-119">In the case of any other command, the call is forwarded without the *dwCrossCodePage* value to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).</span></span>

</dd> <dt>

<span data-ttu-id="c8cf0-120">*dwData* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c8cf0-120">*dwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8cf0-121">Tipo: **DWORD \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="c8cf0-121">Type: **DWORD\_PTR**</span></span>

<span data-ttu-id="c8cf0-122">Cualquier dato que pueda ser necesario, en función del valor del *parámetro uCommand.*</span><span class="sxs-lookup"><span data-stu-id="c8cf0-122">Any data that may be required, based on the value of the *uCommand* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c8cf0-123">*dwCrossCodePage* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c8cf0-123">*dwCrossCodePage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8cf0-124">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c8cf0-124">Type: **DWORD**</span></span>

<span data-ttu-id="c8cf0-125">Valor **DWORD que** indica la página de códigos de la configuración actual del idioma de la interfaz de usuario, como CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="c8cf0-125">The **DWORD** value indicating the code page of the current UI language setting, such as CP\_ACP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8cf0-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8cf0-126">Return value</span></span>

<span data-ttu-id="c8cf0-127">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="c8cf0-127">Type: **HWND**</span></span>

<span data-ttu-id="c8cf0-128">Según el *uCommand* y el resultado especificados, **MLHtmlHelp** devuelve uno o ambos de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="c8cf0-128">Depending on the specified *uCommand* and the result, **MLHtmlHelp** returns one or both of the following:</span></span>

-   <span data-ttu-id="c8cf0-129">Identificador (hwnd) de la ventana de ayuda.</span><span class="sxs-lookup"><span data-stu-id="c8cf0-129">The handle (hwnd) of the help window.</span></span>
-   <span data-ttu-id="c8cf0-130">**NULL**.</span><span class="sxs-lookup"><span data-stu-id="c8cf0-130">**NULL**.</span></span> <span data-ttu-id="c8cf0-131">En algunos casos, **NULL** indica un error; En otros casos, **NULL** indica que aún no se ha creado la ventana de ayuda.</span><span class="sxs-lookup"><span data-stu-id="c8cf0-131">In some cases, **NULL** indicates failure; in other cases, **NULL** indicates that the help window has not yet been created.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8cf0-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8cf0-132">Remarks</span></span>

<span data-ttu-id="c8cf0-133">Si surge un problema con la ruta de acceso del archivo de ayuda para el idioma actual, la llamada se reenvía a [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) para el control estándar.</span><span class="sxs-lookup"><span data-stu-id="c8cf0-133">If a problem arises with the path of the help file for the current language, the call is forwarded to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) for standard handling.</span></span>

<span data-ttu-id="c8cf0-134">Cuando se cierra la ventana de ayuda, el foco vuelve al propietario a menos que el propietario sea el escritorio.</span><span class="sxs-lookup"><span data-stu-id="c8cf0-134">When the help window is closed, focus returns to the owner unless the owner is the desktop.</span></span> <span data-ttu-id="c8cf0-135">Si *hwndCaller es* el escritorio, el sistema operativo determina dónde se devuelve el foco.</span><span class="sxs-lookup"><span data-stu-id="c8cf0-135">If *hwndCaller* is the desktop, then the operating system determines where focus is returned.</span></span>

<span data-ttu-id="c8cf0-136">Además, si **MLHtmlHelp** envía mensajes de notificación desde la ventana de ayuda, los mensajes [](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) se envían a *hwndCaller* siempre que haya habilitado el seguimiento de mensajes de notificación en la definición de la ventana de ayuda.</span><span class="sxs-lookup"><span data-stu-id="c8cf0-136">In addition, if **MLHtmlHelp** sends any notification messages from the help window, the messages are sent to *hwndCaller* as long as you have enabled [notification message](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) tracking in the help window definition.</span></span>

## <a name="examples"></a><span data-ttu-id="c8cf0-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c8cf0-137">Examples</span></span>

<span data-ttu-id="c8cf0-138">En el ejemplo siguiente se llama al comando [HH \_ DISPLAY \_ TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) para abrir el archivo de ayuda denominado Help.chm y mostrar su tema predeterminado en la ventana de ayuda denominada `Mainwin` .</span><span class="sxs-lookup"><span data-stu-id="c8cf0-138">The following example calls the [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) command to open the help file named Help.chm and display its default topic in the help window named `Mainwin`.</span></span> <span data-ttu-id="c8cf0-139">Por lo general, la ventana de ayuda especificada en este comando es un Visor [de Ayuda HTML estándar.](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics)</span><span class="sxs-lookup"><span data-stu-id="c8cf0-139">Generally, the help window specified in this command is a standard [HTML Help Viewer](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics).</span></span>

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> <span data-ttu-id="c8cf0-140">Al usar esta función, establezca el tamaño de pila del ejecutable de hospedaje en al menos 100 000.</span><span class="sxs-lookup"><span data-stu-id="c8cf0-140">When using this function, set the stack size of the hosting executable to at least 100k.</span></span> <span data-ttu-id="c8cf0-141">Si el tamaño de pila definido es demasiado pequeño, el subproceso creado para ejecutar la Ayuda HTML también se creará con este tamaño de pila y la operación podría producir un error.</span><span class="sxs-lookup"><span data-stu-id="c8cf0-141">If the defined stack size is too small, then the thread created to run HTML Help will also be created with this stack size, and the operation could fail.</span></span> <span data-ttu-id="c8cf0-142">Opcionalmente, puede quitar /STACK de la línea de comandos del vínculo y también quitar cualquier configuración stack en el archivo DEF del ejecutable (el tamaño de pila predeterminado es 1 MB en este caso).</span><span class="sxs-lookup"><span data-stu-id="c8cf0-142">Optionally, you can remove /STACK from the link command line, and also remove any STACK setting in the executable's DEF file (default stack size is 1MB in this case).</span></span> <span data-ttu-id="c8cf0-143">También puede establecer el tamaño de pila mediante el comando del compilador /Fnumber (el compilador lo pasará al vinculador como /STACK).</span><span class="sxs-lookup"><span data-stu-id="c8cf0-143">You can also set the stack size using the /Fnumber compiler command (the compiler will pass this to the linker as /STACK).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c8cf0-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8cf0-144">Requirements</span></span>



| <span data-ttu-id="c8cf0-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8cf0-145">Requirement</span></span> | <span data-ttu-id="c8cf0-146">Value</span><span class="sxs-lookup"><span data-stu-id="c8cf0-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8cf0-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8cf0-147">Minimum supported client</span></span><br/> | <span data-ttu-id="c8cf0-148">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="c8cf0-148">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8cf0-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8cf0-149">Minimum supported server</span></span><br/> | <span data-ttu-id="c8cf0-150">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8cf0-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c8cf0-151">Header</span><span class="sxs-lookup"><span data-stu-id="c8cf0-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8cf0-152"><dt>Ninguno</dt></span><span class="sxs-lookup"><span data-stu-id="c8cf0-152"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="c8cf0-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8cf0-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8cf0-154"><dt>Shlwapi.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c8cf0-154"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="c8cf0-155">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="c8cf0-155">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c8cf0-156">**MLHtmlHelpW** (Unicode) y **MLHtmlHelpA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c8cf0-156">**MLHtmlHelpW** (Unicode) and **MLHtmlHelpA** (ANSI)</span></span><br/>                                               |



 

 
