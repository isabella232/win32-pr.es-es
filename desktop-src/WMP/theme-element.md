---
title: Elemento THEME
description: Elemento THEME
ms.assetid: fe7e793e-1774-412c-aed2-721ed2cf1bb3
keywords:
- Aspectos de Windows Media Player, elemento THEME
- máscaras, elemento de tema
- Elemento THEME
- referencia de las máscaras, elemento de tema
- elementos, tema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cd0d40b4b020cf5416569417401af9e4f3a33b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903282"
---
# <a name="theme-element"></a><span data-ttu-id="1a95f-108">Elemento THEME</span><span class="sxs-lookup"><span data-stu-id="1a95f-108">THEME Element</span></span>

<span data-ttu-id="1a95f-109">El elemento de **tema** es el elemento de nivel primario de una máscara y contiene uno o varios elementos de **vista** que, a su vez, contienen todos los demás elementos de una máscara.</span><span class="sxs-lookup"><span data-stu-id="1a95f-109">The **THEME** element is the parent-level element of a skin, and contains one or more **VIEW** elements, which in turn contain all other elements within a skin.</span></span> <span data-ttu-id="1a95f-110">En el código de script, se tiene acceso al elemento de **tema** mediante el atributo global de **tema** en lugar de un nombre especificado por un atributo de **identificador** , que no es compatible con el elemento de **tema** .</span><span class="sxs-lookup"><span data-stu-id="1a95f-110">Within script code, the **THEME** element is accessed through the **theme** global attribute rather than through a name specified by an **id** attribute, which is not supported by the **THEME** element.</span></span>

<span data-ttu-id="1a95f-111">El elemento **Theme** admite los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="1a95f-111">The **THEME** element supports the following attributes.</span></span>



| <span data-ttu-id="1a95f-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="1a95f-112">Attribute</span></span>                                | <span data-ttu-id="1a95f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="1a95f-113">Description</span></span>                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a95f-114">frente</span><span class="sxs-lookup"><span data-stu-id="1a95f-114">author</span></span>](theme-author.md)               | <span data-ttu-id="1a95f-115">Especifica o recupera el nombre del autor de la máscara.</span><span class="sxs-lookup"><span data-stu-id="1a95f-115">Specifies or retrieves the name of the author of the skin.</span></span>                                                                      |
| [<span data-ttu-id="1a95f-116">authorVersion</span><span class="sxs-lookup"><span data-stu-id="1a95f-116">authorVersion</span></span>](theme-authorversion.md) | <span data-ttu-id="1a95f-117">Especifica o recupera el número de versión de la máscara tal como la asigna el autor.</span><span class="sxs-lookup"><span data-stu-id="1a95f-117">Specifies or retrieves the version number of the skin as assigned by the author.</span></span>                                                |
| [<span data-ttu-id="1a95f-118">sSoftware</span><span class="sxs-lookup"><span data-stu-id="1a95f-118">copyright</span></span>](theme-copyright.md)         | <span data-ttu-id="1a95f-119">Especifica o recupera la cadena de copyright de la máscara.</span><span class="sxs-lookup"><span data-stu-id="1a95f-119">Specifies or retrieves the copyright string for the skin.</span></span>                                                                       |
| [<span data-ttu-id="1a95f-120">currentViewID</span><span class="sxs-lookup"><span data-stu-id="1a95f-120">currentViewID</span></span>](theme-currentviewid.md) | <span data-ttu-id="1a95f-121">Especifica o recupera la **vista** mostrada actualmente.</span><span class="sxs-lookup"><span data-stu-id="1a95f-121">Specifies or retrieves the currently displayed **VIEW**.</span></span>                                                                        |
| [<span data-ttu-id="1a95f-122">title</span><span class="sxs-lookup"><span data-stu-id="1a95f-122">title</span></span>](theme-title.md)                 | <span data-ttu-id="1a95f-123">Especifica o recupera el título de la máscara.</span><span class="sxs-lookup"><span data-stu-id="1a95f-123">Specifies or retrieves the title of the skin.</span></span>                                                                                   |
| [<span data-ttu-id="1a95f-124">version</span><span class="sxs-lookup"><span data-stu-id="1a95f-124">version</span></span>](theme-version.md)             | <span data-ttu-id="1a95f-125">Especifica o recupera el número de versión de Windows Media Player para el que se creó la máscara.</span><span class="sxs-lookup"><span data-stu-id="1a95f-125">Specifies or retrieves the Windows Media Player version number for which the skin was authored.</span></span> <span data-ttu-id="1a95f-126">Solo se puede establecer en tiempo de diseño.</span><span class="sxs-lookup"><span data-stu-id="1a95f-126">Can only be set at design time.</span></span> |



 

<span data-ttu-id="1a95f-127">El elemento **Theme** admite los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="1a95f-127">The **THEME** element supports the following methods.</span></span>



| <span data-ttu-id="1a95f-128">Método</span><span class="sxs-lookup"><span data-stu-id="1a95f-128">Method</span></span>                                         | <span data-ttu-id="1a95f-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="1a95f-129">Description</span></span>                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a95f-130">closeView</span><span class="sxs-lookup"><span data-stu-id="1a95f-130">closeView</span></span>](theme-closeview.md)               | <span data-ttu-id="1a95f-131">Cierra una **vista** abierta.</span><span class="sxs-lookup"><span data-stu-id="1a95f-131">Closes an open **VIEW**.</span></span>                                                                                        |
| [<span data-ttu-id="1a95f-132">loadPreference</span><span class="sxs-lookup"><span data-stu-id="1a95f-132">loadPreference</span></span>](theme-loadpreference.md)     | <span data-ttu-id="1a95f-133">Carga una preferencia del registro.</span><span class="sxs-lookup"><span data-stu-id="1a95f-133">Loads a preference from the registry.</span></span>                                                                           |
| [<span data-ttu-id="1a95f-134">logString</span><span class="sxs-lookup"><span data-stu-id="1a95f-134">logString</span></span>](theme-logstring.md)               | <span data-ttu-id="1a95f-135">Registra una cadena definida por el usuario en el archivo de error si está habilitado el registro.</span><span class="sxs-lookup"><span data-stu-id="1a95f-135">Logs a user-defined string to the error file, if logging is enabled.</span></span>                                            |
| [<span data-ttu-id="1a95f-136">openDialog</span><span class="sxs-lookup"><span data-stu-id="1a95f-136">openDialog</span></span>](theme-opendialog.md)             | <span data-ttu-id="1a95f-137">Abre un cuadro de diálogo de archivo.</span><span class="sxs-lookup"><span data-stu-id="1a95f-137">Opens a file dialog box.</span></span>                                                                                        |
| [<span data-ttu-id="1a95f-138">AbrirVista</span><span class="sxs-lookup"><span data-stu-id="1a95f-138">openView</span></span>](theme-openview.md)                 | <span data-ttu-id="1a95f-139">Abre una **vista** en una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="1a95f-139">Opens a **VIEW** in a new window.</span></span>                                                                               |
| [<span data-ttu-id="1a95f-140">openViewRelative</span><span class="sxs-lookup"><span data-stu-id="1a95f-140">openViewRelative</span></span>](theme-openviewrelative.md) | <span data-ttu-id="1a95f-141">Abre una **vista** en una nueva ventana en la posición inicial especificada relativa a la esquina superior izquierda de la máscara.</span><span class="sxs-lookup"><span data-stu-id="1a95f-141">Opens a **VIEW** in a new window at a specified initial position relative to the upper-left corner of the skin.</span></span> |
| [<span data-ttu-id="1a95f-142">Reproducción</span><span class="sxs-lookup"><span data-stu-id="1a95f-142">playSound</span></span>](theme-playsound.md)               | <span data-ttu-id="1a95f-143">Reproduce el archivo de sonido especificado.</span><span class="sxs-lookup"><span data-stu-id="1a95f-143">Plays the specified sound file.</span></span>                                                                                 |
| [<span data-ttu-id="1a95f-144">savePreference</span><span class="sxs-lookup"><span data-stu-id="1a95f-144">savePreference</span></span>](theme-savepreference.md)     | <span data-ttu-id="1a95f-145">Guarda una preferencia en el registro.</span><span class="sxs-lookup"><span data-stu-id="1a95f-145">Saves a preference in the registry.</span></span>                                                                             |
| [<span data-ttu-id="1a95f-146">showErrorDialog</span><span class="sxs-lookup"><span data-stu-id="1a95f-146">showErrorDialog</span></span>](theme-showerrordialog.md)   | <span data-ttu-id="1a95f-147">Muestra el cuadro de diálogo de error estándar.</span><span class="sxs-lookup"><span data-stu-id="1a95f-147">Displays the standard error dialog box.</span></span>                                                                         |



 

<span data-ttu-id="1a95f-148">El elemento **Theme** no admite controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="1a95f-148">The **THEME** element does not support event handlers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a95f-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1a95f-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a95f-150">**Referencia de programación de máscara**</span><span class="sxs-lookup"><span data-stu-id="1a95f-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




