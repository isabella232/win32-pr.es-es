---
description: Windows Installer proporciona a los desarrolladores de paquetes la capacidad de crear una interfaz de usuario interna que tenga varios niveles de funcionalidad.
ms.assetid: 9f5796a7-e244-4fc8-af85-52a147bb2c0b
title: Niveles de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a835d1b11a4db4393041e83c1b1dc885018610f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279322"
---
# <a name="user-interface-levels"></a><span data-ttu-id="0f05c-103">Niveles de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="0f05c-103">User Interface Levels</span></span>

<span data-ttu-id="0f05c-104">Windows Installer proporciona a los desarrolladores de paquetes la capacidad de crear una interfaz de usuario interna que tenga varios niveles de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="0f05c-104">Windows Installer provides package developers the capability to author an internal user interface that has multiple levels of functionality.</span></span> <span data-ttu-id="0f05c-105">Dado que el autor del paquete debe crear la interfaz de usuario interna, el comportamiento de la interfaz de usuario completa, la interfaz de usuario reducida, la interfaz de usuario básica y el nivel ninguno depende del paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="0f05c-105">Because the internal UI must be created by the author of the package, the behavior of the full UI, reduced UI, basic UI, and None levels depends on the installation package.</span></span> <span data-ttu-id="0f05c-106">En la tabla siguiente se describe la funcionalidad que se suele atribuir a los niveles de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="0f05c-106">The following table describes the functionality commonly ascribed to UI levels.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0f05c-107">Nivel de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="0f05c-107">UI Level</span></span></th>
<th><span data-ttu-id="0f05c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f05c-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f05c-109">Interfaz de usuario completa</span><span class="sxs-lookup"><span data-stu-id="0f05c-109">Full UI</span></span></td>
<td><span data-ttu-id="0f05c-110">Muestra cuadros de diálogo modales y no modales creados en la interfaz de usuario interna.</span><span class="sxs-lookup"><span data-stu-id="0f05c-110">Displays modal and modeless dialog boxes that have been authored into the internal UI.</span></span> <span data-ttu-id="0f05c-111">Muestra cuadros de <a href="error-dialog.md">diálogo de error</a> creados.</span><span class="sxs-lookup"><span data-stu-id="0f05c-111">Displays authored <a href="error-dialog.md">Error Dialog</a> boxes.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="0f05c-112">Los cuadros de diálogo modales requieren la intervención del usuario antes de que la instalación pueda continuar y se especifican estableciendo el <a href="modal-dialog-style-bit.md">bit de estilo del cuadro de diálogo modal</a> en la columna atributos de la tabla del <a href="dialog-table.md">cuadro de diálogo</a> .</span><span class="sxs-lookup"><span data-stu-id="0f05c-112">Modal dialog boxes require user input before the installation can continue and are specified by setting the <a href="modal-dialog-style-bit.md">Modal Dialog Style Bit</a> in the Attributes column of the <a href="dialog-table.md">Dialog</a> table.</span></span> <span data-ttu-id="0f05c-113">Un cuadro de diálogo no modal no requiere la intervención del usuario para que la instalación continúe.</span><span class="sxs-lookup"><span data-stu-id="0f05c-113">A modeless dialog box does not require user input for the installation to continue.</span></span>
</blockquote>
<br/> <span data-ttu-id="0f05c-114">Una interfaz de usuario completa normalmente exhibe el <a href="user-interface-wizard-behavior.md">comportamiento del Asistente para la interfaz de usuario</a>.</span><span class="sxs-lookup"><span data-stu-id="0f05c-114">A full UI commonly exhibits <a href="user-interface-wizard-behavior.md">User Interface Wizard Behavior</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f05c-115">Interfaz de usuario reducida</span><span class="sxs-lookup"><span data-stu-id="0f05c-115">Reduced UI</span></span></td>
<td><span data-ttu-id="0f05c-116">Muestra los cuadros de diálogo no modales creados en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="0f05c-116">Displays any modeless dialog boxes that have been authored into the UI.</span></span> <span data-ttu-id="0f05c-117">No muestra ningún cuadro de diálogo modal creado.</span><span class="sxs-lookup"><span data-stu-id="0f05c-117">Does not display any authored modal dialog boxes.</span></span> <span data-ttu-id="0f05c-118">Muestra cuadros de <a href="error-dialog.md">diálogo de error</a> creados.</span><span class="sxs-lookup"><span data-stu-id="0f05c-118">Displays authored <a href="error-dialog.md">Error Dialog</a> boxes.</span></span> <span data-ttu-id="0f05c-119">Muestra mensajes de <a href="authoring-disk-prompt-messages.md">petición de disco</a> .</span><span class="sxs-lookup"><span data-stu-id="0f05c-119">Displays <a href="authoring-disk-prompt-messages.md">Disk Prompt</a> messages.</span></span> <span data-ttu-id="0f05c-120">Muestra cuadros de <a href="filesinuse-dialog.md">diálogo de FilesInUse</a> .</span><span class="sxs-lookup"><span data-stu-id="0f05c-120">Displays <a href="filesinuse-dialog.md">FilesInUse Dialog</a> boxes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f05c-121">Interfaz de usuario básica</span><span class="sxs-lookup"><span data-stu-id="0f05c-121">Basic UI</span></span></td>
<td><span data-ttu-id="0f05c-122">Muestra los cuadros de diálogo no modales integrados que muestran mensajes de progreso.</span><span class="sxs-lookup"><span data-stu-id="0f05c-122">Displays the built-in modeless dialog boxes that show progress messages.</span></span> <span data-ttu-id="0f05c-123">Muestra cuadros de diálogo de error integrados.</span><span class="sxs-lookup"><span data-stu-id="0f05c-123">Displays built-in error dialog boxes.</span></span> <span data-ttu-id="0f05c-124">No muestra ningún cuadro de diálogo creado.</span><span class="sxs-lookup"><span data-stu-id="0f05c-124">Does not display any authored dialog boxes.</span></span> <span data-ttu-id="0f05c-125">Solicita a los usuarios que inserten un disco mostrando un cuadro de diálogo que contiene el valor de la propiedad <a href="diskprompt.md"><strong>DiskPrompt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0f05c-125">Prompts users to insert a disk by displaying a dialog box containing the <a href="diskprompt.md"><strong>DiskPrompt</strong></a> property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f05c-126">None</span><span class="sxs-lookup"><span data-stu-id="0f05c-126">None</span></span></td>
<td><span data-ttu-id="0f05c-127">Ninguno significa una instalación silenciosa que no muestra ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="0f05c-127">None means a silent installation that displays no UI.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0f05c-128">El nivel de la interfaz de usuario interna se puede establecer mediante [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span><span class="sxs-lookup"><span data-stu-id="0f05c-128">The level of the internal UI can be set using [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="0f05c-129">El instalador establece la propiedad [**elemento uilevel**](uilevel.md) en el nivel actual de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="0f05c-129">The installer sets the [**UILevel**](uilevel.md) property to the current level of the UI.</span></span>

<span data-ttu-id="0f05c-130">Si se establece la propiedad [**LIMITUI**](limitui.md) , el nivel de la interfaz de usuario (UI) que se usa al instalar el paquete está restringido a básico.</span><span class="sxs-lookup"><span data-stu-id="0f05c-130">If the [**LIMITUI**](limitui.md) property is set, the user interface (UI) level used when installing the package is restricted to Basic.</span></span>

<span data-ttu-id="0f05c-131">Para obtener un ejemplo de creación de la interfaz de usuario, vea [un ejemplo de instalación](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="0f05c-131">For an example of UI authoring, see [An Installation Example](an-installation-example.md).</span></span>

 

 




