---
description: Para generar un módulo de combinación, debe obtener una herramienta de software con la que editar un archivo. msm.
ms.assetid: bc14d36a-b299-4c61-ade2-43fad142d21d
title: Obtener herramientas de creación de módulos de fusión mediante combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dac673c7cfa191cecb1b576e1b17f2f4a7a1f4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677533"
---
# <a name="obtaining-merge-module-authoring-tools"></a><span data-ttu-id="e270a-103">Obtener herramientas de creación de módulos de fusión mediante combinación</span><span class="sxs-lookup"><span data-stu-id="e270a-103">Obtaining Merge Module Authoring Tools</span></span>

<span data-ttu-id="e270a-104">Para generar un módulo de combinación, debe obtener una herramienta de software con la que editar un archivo. msm.</span><span class="sxs-lookup"><span data-stu-id="e270a-104">To generate a merge module, you need to obtain a software tool with which to edit an .msm file.</span></span> <span data-ttu-id="e270a-105">Dado que un archivo. MSM es básicamente un archivo. msi simplificado, es posible que pueda usar las mismas herramientas que se usan para crear una base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="e270a-105">Because an .msm file is basically a simplified .msi file, you may be able to use the same tools used to create an installation database.</span></span> <span data-ttu-id="e270a-106">Por ejemplo, la aplicación Orca.exe proporciona con el SDK de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e270a-106">For example, the application Orca.exe provided with the Windows Installer SDK.</span></span>

<span data-ttu-id="e270a-107">Una alternativa es adquirir una de las herramientas de empaquetado del instalador para que esté disponible en proveedores de software independientes.</span><span class="sxs-lookup"><span data-stu-id="e270a-107">An alternative is to purchase one of the installer packaging tools to be available from independent software vendors.</span></span> <span data-ttu-id="e270a-108">Hay varias herramientas de terceros en desarrollo que se pueden usar para generar módulos de combinación.</span><span class="sxs-lookup"><span data-stu-id="e270a-108">There are several third-party tools under development that may be used for producing merge modules.</span></span> <span data-ttu-id="e270a-109">Si decide usar una herramienta de terceros, debe comprobar que genera módulos de combinación que son coherentes con el estándar descrito en este documento.</span><span class="sxs-lookup"><span data-stu-id="e270a-109">If you choose to use a third-party tool you should verify that it generates merge modules that are consistent with the standard described in this document.</span></span> <span data-ttu-id="e270a-110">En concreto, debe determinar que las herramientas de edición no han realizado ninguno de los elementos siguientes en el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="e270a-110">In particular, you should determine that the editing tools have not done any of the following to the merge module.</span></span>

-   <span data-ttu-id="e270a-111">Se han agregado tablas extrañas al módulo de combinación al que no se hace referencia en la [tabla ModuleIgnoreTable](moduleignoretable-table.md).</span><span class="sxs-lookup"><span data-stu-id="e270a-111">Added extraneous tables to the merge module that are not referenced in the [ModuleIgnoreTable table](moduleignoretable-table.md).</span></span>

    <span data-ttu-id="e270a-112">Elimine estas tablas o agréguelas a la tabla ModuleIgnoreTable.</span><span class="sxs-lookup"><span data-stu-id="e270a-112">Delete these tables or add them to the ModuleIgnoreTable table.</span></span>

-   <span data-ttu-id="e270a-113">Se ha agregado una [tabla TextStyle](textstyle-table.md) no necesaria al módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="e270a-113">Added an unnecessary [TextStyle table](textstyle-table.md) to the merge module.</span></span>

    <span data-ttu-id="e270a-114">Si el módulo de combinación no tiene ninguna interfaz de usuario (y generalmente no debería hacerlo) puede eliminar esta tabla de forma segura.</span><span class="sxs-lookup"><span data-stu-id="e270a-114">If your merge module has no UI (and it generally should not) you can safely delete this table.</span></span>

-   <span data-ttu-id="e270a-115">Se han agregado entradas innecesarias a la [tabla de directorio](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="e270a-115">Added unnecessary entries to the [Directory table](directory-table.md).</span></span>

    <span data-ttu-id="e270a-116">Quite las entradas innecesarias de la tabla de directorio.</span><span class="sxs-lookup"><span data-stu-id="e270a-116">Remove unnecessary entries from the Directory table.</span></span>

-   <span data-ttu-id="e270a-117">Información izquierda de la tabla de validación del módulo de combinación \_ .</span><span class="sxs-lookup"><span data-stu-id="e270a-117">Left information out of the merge module's \_Validation table.</span></span>

    <span data-ttu-id="e270a-118">Esto evita la validación del módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="e270a-118">This prevents merge module validation.</span></span> <span data-ttu-id="e270a-119">Agregue una \_ tabla de validación completa.</span><span class="sxs-lookup"><span data-stu-id="e270a-119">Add a complete \_Validation table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e270a-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e270a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e270a-121">Crear interfaces de usuario en módulos de combinación</span><span class="sxs-lookup"><span data-stu-id="e270a-121">Authoring User Interfaces in Merge Modules</span></span>](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="e270a-122">Crear tablas del directorio del módulo de combinación</span><span class="sxs-lookup"><span data-stu-id="e270a-122">Authoring Merge Module Directory Tables</span></span>](authoring-merge-module-directory-tables.md)
</dt> <dt>

[<span data-ttu-id="e270a-123">Validar módulos de combinación</span><span class="sxs-lookup"><span data-stu-id="e270a-123">Validating Merge Modules</span></span>](validating-merge-modules.md)
</dt> </dl>

 

 



