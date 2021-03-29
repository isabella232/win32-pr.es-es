---
title: Compatibilidad de localización con controles comunes
description: En este tema se describe la compatibilidad con idiomas nacionales integrados en los controles comunes.
ms.assetid: c5720198-9071-4213-8dad-50b4c015c5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ccc307defa687c8640425dd781660641fe78a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994021"
---
# <a name="localization-support-for-common-controls"></a><span data-ttu-id="c3cc6-103">Compatibilidad de localización con controles comunes</span><span class="sxs-lookup"><span data-stu-id="c3cc6-103">Localization Support for Common Controls</span></span>

<span data-ttu-id="c3cc6-104">En este tema se describe la compatibilidad con idiomas nacionales integrados en los controles comunes.</span><span class="sxs-lookup"><span data-stu-id="c3cc6-104">This topic describes the support for national languages that is built into the common controls.</span></span> <span data-ttu-id="c3cc6-105">La compatibilidad integrada con el lenguaje nacional simplifica la implementación de aplicaciones localizadas.</span><span class="sxs-lookup"><span data-stu-id="c3cc6-105">The built-in national language support simplifies the implementation of localized applications.</span></span>

<span data-ttu-id="c3cc6-106">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="c3cc6-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="c3cc6-107">Especificar un idioma para los controles comunes</span><span class="sxs-lookup"><span data-stu-id="c3cc6-107">Specifying a Language for the Common Controls</span></span>](#specifying-a-language-for-the-common-controls)
-   [<span data-ttu-id="c3cc6-108">Especificar un idioma para los controles de un cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="c3cc6-108">Specifying a Language for Controls in a Dialog Box</span></span>](#specifying-a-language-for-controls-in-a-dialog-box)
-   [<span data-ttu-id="c3cc6-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c3cc6-109">Related topics</span></span>](#related-topics)

## <a name="specifying-a-language-for-the-common-controls"></a><span data-ttu-id="c3cc6-110">Especificar un idioma para los controles comunes</span><span class="sxs-lookup"><span data-stu-id="c3cc6-110">Specifying a Language for the Common Controls</span></span>

<span data-ttu-id="c3cc6-111">Si desea especificar un idioma para los controles comunes que son diferentes del idioma del sistema, llame a [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span><span class="sxs-lookup"><span data-stu-id="c3cc6-111">If you want to specify a language for the common controls that is different than the system language, call [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span></span> <span data-ttu-id="c3cc6-112">El lenguaje especificado por esta función solo se aplica al proceso desde el que se llama a la función.</span><span class="sxs-lookup"><span data-stu-id="c3cc6-112">The language specified by this function applies only to the process from which the function is called.</span></span>

<span data-ttu-id="c3cc6-113">Para determinar el lenguaje que usan actualmente los controles comunes, llame a [**GetMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage).</span><span class="sxs-lookup"><span data-stu-id="c3cc6-113">To determine the language currently being used by the common controls, call [**GetMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage).</span></span> <span data-ttu-id="c3cc6-114">Devuelve el valor establecido por una llamada anterior a [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span><span class="sxs-lookup"><span data-stu-id="c3cc6-114">It returns the value that was set by a previous call to [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span></span> <span data-ttu-id="c3cc6-115">El lenguaje devuelto es el que se especificó para el proceso del que se llama.</span><span class="sxs-lookup"><span data-stu-id="c3cc6-115">The language returned is the one that was specified for the process it is called from.</span></span> <span data-ttu-id="c3cc6-116">Si no se ha llamado a **InitMUILanguage** o se llamó desde otro proceso, **GetMUILanguage** devolverá un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c3cc6-116">If **InitMUILanguage** has not been called, or was called from another process, **GetMUILanguage** will return a default value.</span></span>

## <a name="specifying-a-language-for-controls-in-a-dialog-box"></a><span data-ttu-id="c3cc6-117">Especificar un idioma para los controles de un cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="c3cc6-117">Specifying a Language for Controls in a Dialog Box</span></span>

<span data-ttu-id="c3cc6-118">A diferencia de los controles comunes, los controles predefinidos como botones o cuadros de edición no usan el idioma actual del sistema de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c3cc6-118">Unlike common controls, predefined controls such as buttons or edit boxes do not use the current system language by default.</span></span> <span data-ttu-id="c3cc6-119">El control de fuentes nativo es un control invisible que funciona en segundo plano para permitir que los controles predefinidos de un cuadro de diálogo muestren el idioma actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="c3cc6-119">The native font control is an invisible control that works in the background to allow a dialog box's predefined controls to display the current system language.</span></span>

<span data-ttu-id="c3cc6-120">Para usar el control de fuente nativo, siga este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="c3cc6-120">To use the native font control, follow this procedure.</span></span>

1.  <span data-ttu-id="c3cc6-121">Inicialice el control de fuentes nativo llamando a [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span><span class="sxs-lookup"><span data-stu-id="c3cc6-121">Initialize the native font control by calling [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span></span> <span data-ttu-id="c3cc6-122">Establezca el miembro **dwICC** de la estructura [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) a la que apunta *lpInitCtrls* a la \_ clase NATIVEFNTCTL de ICC \_ .</span><span class="sxs-lookup"><span data-stu-id="c3cc6-122">Set the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure pointed to by *lpInitCtrls* to ICC\_NATIVEFNTCTL\_CLASS.</span></span>
2.  <span data-ttu-id="c3cc6-123">Agregue el control al script de recursos para el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c3cc6-123">Add the control to the resource script for the dialog box.</span></span> <span data-ttu-id="c3cc6-124">Establezca una o varias de las marcas de estilo siguientes para especificar los controles que se verán afectados.</span><span class="sxs-lookup"><span data-stu-id="c3cc6-124">Set one or more of the following style flags to specify which controls will be affected.</span></span> 

    | <span data-ttu-id="c3cc6-125">Marca</span><span class="sxs-lookup"><span data-stu-id="c3cc6-125">Flag</span></span>              | <span data-ttu-id="c3cc6-126">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="c3cc6-126">Applies to</span></span>                                                                                                                                                                                                                                                       |
    |-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="c3cc6-127">edición de NFS \_</span><span class="sxs-lookup"><span data-stu-id="c3cc6-127">NFS\_EDIT</span></span>         | <span data-ttu-id="c3cc6-128">Controles de edición</span><span class="sxs-lookup"><span data-stu-id="c3cc6-128">Edit controls</span></span>                                                                                                                                                                                                                                                    |
    | <span data-ttu-id="c3cc6-129">estática de NFS \_</span><span class="sxs-lookup"><span data-stu-id="c3cc6-129">NFS\_STATIC</span></span>       | <span data-ttu-id="c3cc6-130">Controles estáticos</span><span class="sxs-lookup"><span data-stu-id="c3cc6-130">Static controls</span></span>                                                                                                                                                                                                                                                  |
    | <span data-ttu-id="c3cc6-131">\_LISTCOMBO NFS</span><span class="sxs-lookup"><span data-stu-id="c3cc6-131">NFS\_LISTCOMBO</span></span>    | <span data-ttu-id="c3cc6-132">Controles List, ComboBox, List-View y ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="c3cc6-132">List, ComboBox, List-View, and ComboBoxEx controls</span></span>                                                                                                                                                                                                               |
    | <span data-ttu-id="c3cc6-133">\_botón NFS</span><span class="sxs-lookup"><span data-stu-id="c3cc6-133">NFS\_BUTTON</span></span>       | <span data-ttu-id="c3cc6-134">Controles de botón</span><span class="sxs-lookup"><span data-stu-id="c3cc6-134">Button controls</span></span>                                                                                                                                                                                                                                                  |
    | <span data-ttu-id="c3cc6-135">\_todo NFS</span><span class="sxs-lookup"><span data-stu-id="c3cc6-135">NFS\_ALL</span></span>          | <span data-ttu-id="c3cc6-136">Todos los controles</span><span class="sxs-lookup"><span data-stu-id="c3cc6-136">All controls</span></span>                                                                                                                                                                                                                                                     |
    | <span data-ttu-id="c3cc6-137">\_USEFONTASSOC NFS</span><span class="sxs-lookup"><span data-stu-id="c3cc6-137">NFS\_USEFONTASSOC</span></span> | <span data-ttu-id="c3cc6-138">Plataforma de Asia oriental.</span><span class="sxs-lookup"><span data-stu-id="c3cc6-138">East Asian platform.</span></span> <span data-ttu-id="c3cc6-139">El control usa la característica de Asociación de fuentes en lugar de cambiar a la fuente nativa.</span><span class="sxs-lookup"><span data-stu-id="c3cc6-139">The control uses the font association feature instead of switching to the native font.</span></span> <span data-ttu-id="c3cc6-140">Todas las demás plataformas lo omiten.</span><span class="sxs-lookup"><span data-stu-id="c3cc6-140">All other platforms ignore it.</span></span> <span data-ttu-id="c3cc6-141">Esto está en desuso para Windows Vista y no se admite en comctl V6.</span><span class="sxs-lookup"><span data-stu-id="c3cc6-141">This is deprecated for Windows Vista, and is not supported in comctl v6.</span></span> <span data-ttu-id="c3cc6-142">Esto existe en comctl V5 por motivos de herencia.</span><span class="sxs-lookup"><span data-stu-id="c3cc6-142">This exists in comctl v5 for legacy reasons.</span></span> |

    

     

<span data-ttu-id="c3cc6-143">En el ejemplo siguiente se muestra cómo agregar un control de fuente nativo a un script de recursos.</span><span class="sxs-lookup"><span data-stu-id="c3cc6-143">The following example illustrates how to add a native font control to a resource script.</span></span> <span data-ttu-id="c3cc6-144">Hace que los controles de edición, lista y cuadro combinado del cuadro de diálogo muestren texto con el idioma actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="c3cc6-144">It causes the dialog box's edit, list, and combo box controls to display text using the current system language.</span></span>


```
CONTROL    "",-1,"NativeFontCtl",NFS_EDIT|NFS_LISTCOMBO,0,0,0,0
```



## <a name="related-topics"></a><span data-ttu-id="c3cc6-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c3cc6-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3cc6-146">Acerca de los controles comunes</span><span class="sxs-lookup"><span data-stu-id="c3cc6-146">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 




