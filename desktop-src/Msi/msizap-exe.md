---
description: Msizap.exe es una utilidad de línea de comandos que quita toda la información Windows Installer de un producto o de todos los productos instalados en un equipo. Es posible que los productos instalados por el instalador no funcionen después de usar Msizap.
ms.assetid: 0debb8ab-3ae7-447e-84fc-0466ec1b2f26
title: Msizap.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a89f2287443bc442ee767b01e975d6bcc118c1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082462"
---
# <a name="msizapexe"></a><span data-ttu-id="36d4c-104">Msizap.exe</span><span class="sxs-lookup"><span data-stu-id="36d4c-104">Msizap.exe</span></span>

<span data-ttu-id="36d4c-105">Msizap.exe es una utilidad de línea de comandos que quita toda la información Windows Installer de un producto o de todos los productos instalados en un equipo.</span><span class="sxs-lookup"><span data-stu-id="36d4c-105">Msizap.exe is a command line utility that removes either all Windows Installer information for a product or all products installed on a computer.</span></span> <span data-ttu-id="36d4c-106">Es posible que los productos instalados por el instalador no funcionen después de usar Msizap.</span><span class="sxs-lookup"><span data-stu-id="36d4c-106">Products installed by the installer may fail to function after using Msizap.</span></span>

<span data-ttu-id="36d4c-107">En Windows 2000 y Windows XP, se necesitan privilegios administrativos para usar Msizap.exe.</span><span class="sxs-lookup"><span data-stu-id="36d4c-107">On Windows 2000 and Windows XP, administrative privileges are required to use Msizap.exe.</span></span>

<span data-ttu-id="36d4c-108">Esta herramienta solo está disponible en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md) y no se debe redistribuir.</span><span class="sxs-lookup"><span data-stu-id="36d4c-108">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) and should not be redistributed.</span></span> <span data-ttu-id="36d4c-109">Use la versión reciente de Msizap.exe (versión 3.1.4000.2726 o superior) que está disponible en los componentes de Windows SDK para Windows Installer desarrolladores de Windows Vista o superior.</span><span class="sxs-lookup"><span data-stu-id="36d4c-109">Use the recent version of Msizap.exe (version 3.1.4000.2726 or greater) that is available in the Windows SDK Components for Windows Installer Developers for Windows Vista or greater.</span></span> <span data-ttu-id="36d4c-110">Las versiones inferiores de Msizap.exe pueden quitar información acerca de todas las actualizaciones que se han aplicado a otras aplicaciones en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="36d4c-110">Lesser versions of Msizap.exe can remove information about all updates that have been applied to other applications on the user's computer.</span></span> <span data-ttu-id="36d4c-111">Si se quita esta información, es posible que sea necesario quitar y volver a instalar estas otras aplicaciones para recibir actualizaciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="36d4c-111">If this information is removed, these other applications may need to be removed and reinstalled to receive additional updates.</span></span>

## <a name="syntax"></a><span data-ttu-id="36d4c-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36d4c-112">Syntax</span></span>

<span data-ttu-id="36d4c-113">¡ **Msizap T**_\[ wa! \] {código de producto}_</span><span class="sxs-lookup"><span data-stu-id="36d4c-113">**msizap T**_\[WA!\]{product code}_</span></span>

<span data-ttu-id="36d4c-114">¡ **Msizap T**_\[ wa \] <msi package> !_</span><span class="sxs-lookup"><span data-stu-id="36d4c-114">**msizap T**_\[WA!\]<msi package>_</span></span>

<span data-ttu-id="36d4c-115">\**\* \*\*\* Msizap \[ WA \]* **ALLPRODUCTS**</span><span class="sxs-lookup"><span data-stu-id="36d4c-115">\**msizap \*\*\*\*\[WA!\]* **ALLPRODUCTS**</span></span>

<span data-ttu-id="36d4c-116">**PWSA de Msizap?**</span><span class="sxs-lookup"><span data-stu-id="36d4c-116">**msizap PWSA?!**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="36d4c-117">Opciones de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="36d4c-117">Command Line Options</span></span>

<span data-ttu-id="36d4c-118">Msizap.exe usa las opciones de línea de comandos que no distinguen mayúsculas de minúsculas que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="36d4c-118">Msizap.exe uses case-insensitive command line options shown in the following table.</span></span>



| <span data-ttu-id="36d4c-119">Opción</span><span class="sxs-lookup"><span data-stu-id="36d4c-119">Option</span></span> | <span data-ttu-id="36d4c-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="36d4c-120">Description</span></span>                                                                                                                                                                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*     | <span data-ttu-id="36d4c-121">Quita todos los Windows Installer carpetas y claves del registro, ajusta los recuentos de DLL compartidas y detiene Windows Installer servicio.</span><span class="sxs-lookup"><span data-stu-id="36d4c-121">Removes all Windows Installer folders and registry keys, adjusts shared DLL counts, and stops Windows Installer service.</span></span> <span data-ttu-id="36d4c-122">También quita la In-Progress clave y la información de reversión.</span><span class="sxs-lookup"><span data-stu-id="36d4c-122">Also removes the In-Progress key and rollback information.</span></span>                                                                           |
| <span data-ttu-id="36d4c-123">a</span><span class="sxs-lookup"><span data-stu-id="36d4c-123">a</span></span>      | <span data-ttu-id="36d4c-124">Solo cambia las ACL al control total de administración para cualquier eliminación especificada.</span><span class="sxs-lookup"><span data-stu-id="36d4c-124">Only changes ACLs to Admin Full Control for any specified removal.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="36d4c-125">e</span><span class="sxs-lookup"><span data-stu-id="36d4c-125">g</span></span>      | <span data-ttu-id="36d4c-126">Para todos los usuarios, quita todos los archivos de datos Windows Installer almacenados en caché que se hayan huérfano.</span><span class="sxs-lookup"><span data-stu-id="36d4c-126">For all users, removes any cached Windows Installer data files that have been orphaned.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="36d4c-127">p</span><span class="sxs-lookup"><span data-stu-id="36d4c-127">p</span></span>      | <span data-ttu-id="36d4c-128">Quita la clave de In-Progress.</span><span class="sxs-lookup"><span data-stu-id="36d4c-128">Removes the In-Progress key.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="36d4c-129">s</span><span class="sxs-lookup"><span data-stu-id="36d4c-129">s</span></span>      | <span data-ttu-id="36d4c-130">Quita la información de reversión.</span><span class="sxs-lookup"><span data-stu-id="36d4c-130">Removes Rollback Information.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="36d4c-131">t</span><span class="sxs-lookup"><span data-stu-id="36d4c-131">t</span></span>      | <span data-ttu-id="36d4c-132">Quita toda la información del código de producto especificado.</span><span class="sxs-lookup"><span data-stu-id="36d4c-132">Removes all information for the specified product code.</span></span> <span data-ttu-id="36d4c-133">Al usar esta opción, incluya el código de producto entre llaves.</span><span class="sxs-lookup"><span data-stu-id="36d4c-133">When using this option, enclose the Product Code in curly braces.</span></span> <span data-ttu-id="36d4c-134">Esta opción se puede usar con la ruta de acceso completa al archivo. msi o con el código del producto.</span><span class="sxs-lookup"><span data-stu-id="36d4c-134">This option may be used with either the full path to the .msi file or with the product code.</span></span>                                        |
| <span data-ttu-id="36d4c-135">w</span><span class="sxs-lookup"><span data-stu-id="36d4c-135">w</span></span>      | <span data-ttu-id="36d4c-136">Quita Windows Installer información de todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="36d4c-136">Removes Windows Installer information for all users.</span></span> <span data-ttu-id="36d4c-137">Cuando no se establece esta opción, solo se quita la información del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="36d4c-137">When this option is not set, only the information for the current user is removed.</span></span> <span data-ttu-id="36d4c-138">El uso de esta opción requiere que se cargue el perfil del usuario para que el subárbol del registro por usuario del usuario esté disponible.</span><span class="sxs-lookup"><span data-stu-id="36d4c-138">Use of this option requires that the user's profile be loaded so that the user's per-user registry hive be available.</span></span> |
| <span data-ttu-id="36d4c-139">?</span><span class="sxs-lookup"><span data-stu-id="36d4c-139">?</span></span>      | <span data-ttu-id="36d4c-140">Ayuda detallada.</span><span class="sxs-lookup"><span data-stu-id="36d4c-140">Verbose help.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="36d4c-141">!</span><span class="sxs-lookup"><span data-stu-id="36d4c-141">!</span></span>      | <span data-ttu-id="36d4c-142">Fuerza una respuesta "sí" a cualquier solicitud.</span><span class="sxs-lookup"><span data-stu-id="36d4c-142">Forces a 'yes' response to any prompt.</span></span>                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="36d4c-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="36d4c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36d4c-144">Versiones publicadas, herramientas y redistribuibles</span><span class="sxs-lookup"><span data-stu-id="36d4c-144">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



