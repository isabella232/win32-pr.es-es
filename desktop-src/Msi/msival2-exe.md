---
description: Msival2.exe es una utilidad de línea de comandos que puede ejecutar un conjunto de evaluadores de coherencia internos, CIEM.
ms.assetid: c48f4584-732a-468d-a651-2c09ce3c9ddd
title: Msival2.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b70ca2ccdeaf72c5191f292a8fa3f9b4de5dd9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279337"
---
# <a name="msival2exe"></a><span data-ttu-id="5a83f-103">Msival2.exe</span><span class="sxs-lookup"><span data-stu-id="5a83f-103">Msival2.exe</span></span>

<span data-ttu-id="5a83f-104">Msival2.exe es una utilidad de línea de comandos que puede ejecutar un conjunto de [evaluadores de coherencia internos, CIEM](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="5a83f-104">Msival2.exe is a command line utility that can run a suite of [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span>

<span data-ttu-id="5a83f-105">Esta herramienta solo está disponible en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="5a83f-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="5a83f-106">Para obtener más información acerca del ICEs y el archivo CUB, consulte [uso de evaluadores de coherencia internos](using-internal-consistency-evaluators.md).</span><span class="sxs-lookup"><span data-stu-id="5a83f-106">For more information about ICEs and the CUB file, see [Using Internal Consistency Evaluators](using-internal-consistency-evaluators.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a83f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a83f-107">Syntax</span></span>

<span data-ttu-id="5a83f-108">**Msival2** *{Database} {Cub file} \[ -f \] \[ -l {logfile} \] \[ -i {Ice ID} \[ : {Ice ID}... \] \]*</span><span class="sxs-lookup"><span data-stu-id="5a83f-108">**Msival2** *{database}{CUB file}\[-f\]\[-l {logfile}\]\[-i {ICE Id}\[:{ICE Id}...\]\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="5a83f-109">Opciones de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="5a83f-109">Command Line Options</span></span>

<span data-ttu-id="5a83f-110">Msival2.exe usa las siguientes opciones de la línea de comandos que no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5a83f-110">Msival2.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="5a83f-111">También se puede usar un delimitador de barra diagonal en lugar de un guión.</span><span class="sxs-lookup"><span data-stu-id="5a83f-111">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="5a83f-112">Opción</span><span class="sxs-lookup"><span data-stu-id="5a83f-112">Option</span></span> | <span data-ttu-id="5a83f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a83f-113">Description</span></span>                                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a83f-114">-f</span><span class="sxs-lookup"><span data-stu-id="5a83f-114">-f</span></span>     | <span data-ttu-id="5a83f-115">Filtre todos los mensajes informativos de los resultados mostrados.</span><span class="sxs-lookup"><span data-stu-id="5a83f-115">Filter out all informational messages from the displayed results.</span></span> <span data-ttu-id="5a83f-116">Se muestran todos los demás tipos de mensajes.</span><span class="sxs-lookup"><span data-stu-id="5a83f-116">All other types of messages are displayed.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="5a83f-117">-i</span><span class="sxs-lookup"><span data-stu-id="5a83f-117">-i</span></span>     | <span data-ttu-id="5a83f-118">Ejecute únicamente el ICEs indicado en la línea de comandos en el orden especificado.</span><span class="sxs-lookup"><span data-stu-id="5a83f-118">Run only the ICEs listed on the command line in the order specified.</span></span> <span data-ttu-id="5a83f-119">Cada acción personalizada ICE debe aparecer tal como aparece en la [tabla CustomAction](customaction-table.md) del archivo Cub.</span><span class="sxs-lookup"><span data-stu-id="5a83f-119">Each ICE custom action should be listed as it appears in the [CustomAction table](customaction-table.md) of the CUB file.</span></span> <span data-ttu-id="5a83f-120">Si se omite esta opción, la herramienta ejecuta el conjunto predeterminado de CIEM especificado por el autor del archivo CUB.</span><span class="sxs-lookup"><span data-stu-id="5a83f-120">If this option is omitted, the tool runs the default set of ICEs specified by the author of the CUB file.</span></span> |
| <span data-ttu-id="5a83f-121">-l</span><span class="sxs-lookup"><span data-stu-id="5a83f-121">-l</span></span>     | <span data-ttu-id="5a83f-122">Escribe los resultados en el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="5a83f-122">Write results to the specified file.</span></span> <span data-ttu-id="5a83f-123">El archivo no debe existir todavía.</span><span class="sxs-lookup"><span data-stu-id="5a83f-123">The file must not already exist.</span></span> <span data-ttu-id="5a83f-124">Si el archivo existe, no se sobrescribe.</span><span class="sxs-lookup"><span data-stu-id="5a83f-124">If the file exists, it is not overwritten.</span></span>                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="5a83f-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5a83f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a83f-126">Herramientas de desarrollo de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="5a83f-126">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="5a83f-127">Evaluadores de coherencia interna-CIEM</span><span class="sxs-lookup"><span data-stu-id="5a83f-127">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)
</dt> <dt>

[<span data-ttu-id="5a83f-128">Versiones publicadas, herramientas y redistribuibles</span><span class="sxs-lookup"><span data-stu-id="5a83f-128">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



