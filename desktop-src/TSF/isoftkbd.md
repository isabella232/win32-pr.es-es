---
title: Interfaz ISoftKbd (Softkbdc. h)
description: Las aplicaciones y los servicios de texto usan la interfaz ISoftKbd para implementar un teclado en pantalla.
ms.assetid: 804634bd-646e-459f-9fbb-cd6929b11fab
keywords:
- ISoftKbd interface Text Services Framework
- ISoftKbd interface Text Services Framework, descrito
topic_type:
- apiref
api_name:
- ISoftKbd
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e046964616fc564aa2e0c3d0098ee2186cdaf8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685849"
---
# <a name="isoftkbd-interface"></a><span data-ttu-id="c0ffa-105">Interfaz ISoftKbd</span><span class="sxs-lookup"><span data-stu-id="c0ffa-105">ISoftKbd interface</span></span>

<span data-ttu-id="c0ffa-106">Las aplicaciones y los servicios de texto usan la interfaz **ISoftKbd** para implementar un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-106">The **ISoftKbd** interface is used by applications and text services to implement a soft keyboard.</span></span>

## <a name="members"></a><span data-ttu-id="c0ffa-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c0ffa-107">Members</span></span>

<span data-ttu-id="c0ffa-108">La interfaz **ISoftKbd** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c0ffa-108">The **ISoftKbd** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c0ffa-109">**ISoftKbd** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c0ffa-109">**ISoftKbd** also has these types of members:</span></span>

-   [<span data-ttu-id="c0ffa-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="c0ffa-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c0ffa-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c0ffa-111">Methods</span></span>

<span data-ttu-id="c0ffa-112">La interfaz **ISoftKbd** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-112">The **ISoftKbd** interface has these methods.</span></span>



| <span data-ttu-id="c0ffa-113">Método</span><span class="sxs-lookup"><span data-stu-id="c0ffa-113">Method</span></span>                                                                                        | <span data-ttu-id="c0ffa-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0ffa-114">Description</span></span>                                                                                                   |
|:----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0ffa-115">**AdviseSoftKeyboardEventSink**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-115">**AdviseSoftKeyboardEventSink**</span></span>](isoftkbd-advisesoftkeyboardeventsink.md)                   | <span data-ttu-id="c0ffa-116">Instala un receptor de eventos de teclado en pantalla para controlar las notificaciones de OnKeySelection desde el teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-116">Installs a soft keyboard event sink to handle OnKeySelection notifications from the soft keyboard.</span></span><br/> |
| [<span data-ttu-id="c0ffa-117">**CreateSoftKeyboardLayoutFromResource**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-117">**CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md) | <span data-ttu-id="c0ffa-118">Crea una distribución de teclado en pantalla a partir del recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-118">Creates a soft keyboard layout from the specified resource.</span></span><br/>                                        |
| [<span data-ttu-id="c0ffa-119">**CreateSoftKeyboardLayoutFromXMLFile**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-119">**CreateSoftKeyboardLayoutFromXMLFile**</span></span>](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)   | <span data-ttu-id="c0ffa-120">Crea una distribución de teclado en pantalla desde el archivo XML especificado.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-120">Creates a soft keyboard layout from the specified XML file.</span></span><br/>                                        |
| [<span data-ttu-id="c0ffa-121">**CreateSoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-121">**CreateSoftKeyboardWindow**</span></span>](isoftkbd-createsoftkeyboardwindow.md)                         | <span data-ttu-id="c0ffa-122">Crea una ventana de teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-122">Creates a soft keyboard window.</span></span><br/>                                                                    |
| [<span data-ttu-id="c0ffa-123">**DestroySoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-123">**DestroySoftKeyboardWindow**</span></span>](isoftkbd-destroysoftkeyboardwindow.md)                       | <span data-ttu-id="c0ffa-124">Destruye una ventana de teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-124">Destroys a soft keyboard window.</span></span><br/>                                                                   |
| [<span data-ttu-id="c0ffa-125">**EnumSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-125">**EnumSoftKeyboard**</span></span>](isoftkbd-enumsoftkeyboard.md)                                         | <span data-ttu-id="c0ffa-126">Enumera los posibles teclados de software que admiten el idioma especificado.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-126">Enumerates the possible soft keyboards that support the specified language.</span></span><br/>                        |
| [<span data-ttu-id="c0ffa-127">**GetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-127">**GetSoftKeyboardColors**</span></span>](isoftkbd-getsoftkeyboardcolors.md)                               | <span data-ttu-id="c0ffa-128">Recupera el color del teclado blando correspondiente al tipo de color proporcionado.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-128">Retrieves the soft keyboard color corresponding to the supplied color type.</span></span><br/>                        |
| [<span data-ttu-id="c0ffa-129">**GetSoftKeyboardPosSize**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-129">**GetSoftKeyboardPosSize**</span></span>](isoftkbd-getsoftkeyboardpossize.md)                             | <span data-ttu-id="c0ffa-130">Recupera la posición inicial y el tamaño de un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-130">Retrieves the starting position and size of a soft keyboard.</span></span><br/>                                       |
| [<span data-ttu-id="c0ffa-131">**GetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-131">**GetSoftKeyboardTextFont**</span></span>](isoftkbd-getsoftkeyboardtextfont.md)                           | <span data-ttu-id="c0ffa-132">Recupera la fuente de texto utilizada por un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-132">Retrieves the text font used by a soft keyboard.</span></span><br/>                                                   |
| [<span data-ttu-id="c0ffa-133">**GetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-133">**GetSoftKeyboardTypeMode**</span></span>](isoftkbd-getsoftkeyboardtypemode.md)                           | <span data-ttu-id="c0ffa-134">Recupera el modo de tipo para un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-134">Retrieves the type mode for a soft keyboard.</span></span><br/>                                                       |
| [<span data-ttu-id="c0ffa-135">**Inicialización**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-135">**Initialize**</span></span>](isoftkbd-initialize.md)                                                     | <span data-ttu-id="c0ffa-136">Inicializa todos los campos necesarios para un teclado en pantalla y genera diseños de teclado en pantalla estándar.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-136">Initializes all necessary fields for a soft keyboard and generates standard soft keyboard layouts.</span></span><br/> |
| [<span data-ttu-id="c0ffa-137">**SelectSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-137">**SelectSoftKeyboard**</span></span>](isoftkbd-selectsoftkeyboard.md)                                     | <span data-ttu-id="c0ffa-138">Selecciona el teclado en pantalla especificado.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-138">Selects the specified soft keyboard.</span></span><br/>                                                               |
| [<span data-ttu-id="c0ffa-139">**SetKeyboardLabelText**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-139">**SetKeyboardLabelText**</span></span>](isoftkbd-setkeyboardlabeltext.md)                                 | <span data-ttu-id="c0ffa-140">Establece el texto de la etiqueta del diseño de un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-140">Sets the label text from the layout for a soft keyboard.</span></span><br/>                                           |
| [<span data-ttu-id="c0ffa-141">**SetKeyboardLabelTextCombination**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-141">**SetKeyboardLabelTextCombination**</span></span>](isoftkbd-setkeyboardlabeltextcombination.md)           | <span data-ttu-id="c0ffa-142">Establece una combinación de etiqueta y texto que se usa para describir un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-142">Sets a combination of label and text used to describe a soft keyboard.</span></span><br/>                             |
| [<span data-ttu-id="c0ffa-143">**SetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-143">**SetSoftKeyboardColors**</span></span>](isoftkbd-setsoftkeyboardcolors.md)                               | <span data-ttu-id="c0ffa-144">Establece el color del teclado blando correspondiente al tipo de color proporcionado.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-144">Sets the soft keyboard color corresponding to the supplied color type.</span></span><br/>                             |
| [<span data-ttu-id="c0ffa-145">**SetSoftKeyboardPosSize**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-145">**SetSoftKeyboardPosSize**</span></span>](isoftkbd-setsoftkeyboardpossize.md)                             | <span data-ttu-id="c0ffa-146">Establece la posición inicial y el tamaño de un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-146">Sets the starting position and size of a soft keyboard.</span></span><br/>                                            |
| [<span data-ttu-id="c0ffa-147">**SetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-147">**SetSoftKeyboardTextFont**</span></span>](isoftkbd-setsoftkeyboardtextfont.md)                           | <span data-ttu-id="c0ffa-148">Establece la fuente de texto utilizada por un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-148">Sets the text font used by a soft keyboard.</span></span><br/>                                                        |
| [<span data-ttu-id="c0ffa-149">**SetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-149">**SetSoftKeyboardTypeMode**</span></span>](isoftkbd-setsoftkeyboardtypemode.md)                           | <span data-ttu-id="c0ffa-150">Establece el modo de tipo para un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-150">Sets the type mode for a soft keyboard.</span></span><br/>                                                            |
| [<span data-ttu-id="c0ffa-151">**ShowKeysForKeyScanMode**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-151">**ShowKeysForKeyScanMode**</span></span>](isoftkbd-showkeysforkeyscanmode.md)                             | <span data-ttu-id="c0ffa-152">Muestra las claves utilizadas para el modo de exploración de teclas para un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-152">Displays the keys used for the key scan mode for a soft keyboard.</span></span><br/>                                  |
| [<span data-ttu-id="c0ffa-153">**ShowSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-153">**ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)                                         | <span data-ttu-id="c0ffa-154">Muestra un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-154">Displays a soft keyboard.</span></span><br/>                                                                          |
| [<span data-ttu-id="c0ffa-155">**UnadviseSoftKeyboardEventSink**</span><span class="sxs-lookup"><span data-stu-id="c0ffa-155">**UnadviseSoftKeyboardEventSink**</span></span>](isoftkbd-unadvisesoftkeyboardeventsink.md)               | <span data-ttu-id="c0ffa-156">Quita un receptor de eventos de teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="c0ffa-156">Removes a soft keyboard event sink.</span></span><br/>                                                                |



 

## <a name="requirements"></a><span data-ttu-id="c0ffa-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0ffa-157">Requirements</span></span>



| <span data-ttu-id="c0ffa-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0ffa-158">Requirement</span></span> | <span data-ttu-id="c0ffa-159">Value</span><span class="sxs-lookup"><span data-stu-id="c0ffa-159">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ffa-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0ffa-160">Minimum supported client</span></span><br/> | <span data-ttu-id="c0ffa-161">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c0ffa-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c0ffa-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0ffa-162">Minimum supported server</span></span><br/> | <span data-ttu-id="c0ffa-163">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c0ffa-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c0ffa-164">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="c0ffa-164">Redistributable</span></span><br/>          | <span data-ttu-id="c0ffa-165">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c0ffa-165">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="c0ffa-166">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0ffa-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0ffa-167"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0ffa-167"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="c0ffa-168">IDL</span><span class="sxs-lookup"><span data-stu-id="c0ffa-168">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c0ffa-169"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c0ffa-169"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="c0ffa-170">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c0ffa-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0ffa-171"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0ffa-171"><dt>Softkbd.dll</dt></span></span> </dl> |



 

