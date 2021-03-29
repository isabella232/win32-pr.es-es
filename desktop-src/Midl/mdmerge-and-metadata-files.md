---
title: Archivos de metadatos y MDMERGE
description: Compone varios archivos de metadatos (. winmd) en una serie de archivos de metadatos de salida, basados en el espacio de nombres.
ms.assetid: A3203627-82DF-4744-BBBC-53D13F30210E
keywords:
- metadata
- archivo winmd
- Metadatos de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2d91f8c7506dd80fd2477beb61c5b99a26b05b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993961"
---
# <a name="mdmerge-and-metadata-files"></a><span data-ttu-id="8b114-106">Archivos de metadatos y MDMERGE</span><span class="sxs-lookup"><span data-stu-id="8b114-106">MDMERGE and metadata files</span></span>

<span data-ttu-id="8b114-107">Compone varios archivos de metadatos (. winmd) en una serie de archivos de metadatos de salida, basados en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="8b114-107">Composes multiple metadata (.winmd) files into a number of output metadata files, based on namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="8b114-108">Uso</span><span class="sxs-lookup"><span data-stu-id="8b114-108">Usage</span></span>

<span data-ttu-id="8b114-109">Ejecute MDMERGE desde la línea de comandos con el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="8b114-109">Run MDMERGE from the command line using the following command:</span></span>

<span data-ttu-id="8b114-110"> *< ***Opciones*** de mdmerge>*</span><span class="sxs-lookup"><span data-stu-id="8b114-110">**mdmerge** *<***options***>*</span></span>

<span data-ttu-id="8b114-111">donde *< ***Options*** >* representa las opciones de línea de comandos que desea utilizar.</span><span class="sxs-lookup"><span data-stu-id="8b114-111">where *<***options***>* represents the command-line options you want to use.</span></span>

<span data-ttu-id="8b114-112">Genere archivos de metadatos para los componentes de Windows Runtime personalizados mediante el compilador MIDLRT.</span><span class="sxs-lookup"><span data-stu-id="8b114-112">Generate metadata files for your custom Windows Runtime components by using the MIDLRT compiler.</span></span> <span data-ttu-id="8b114-113">Para obtener más información, consulte [MIDLRT y Windows Runtime componentes](midlrt-and-windows-runtime-components.md).</span><span class="sxs-lookup"><span data-stu-id="8b114-113">For more info, see [MIDLRT and Windows Runtime components](midlrt-and-windows-runtime-components.md).</span></span>

## <a name="command-line-switches"></a><span data-ttu-id="8b114-114">Modificadores de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="8b114-114">Command-line switches</span></span>

<span data-ttu-id="8b114-115">En la lista siguiente se muestran los modificadores de la línea de comandos que usa MDMERGE.</span><span class="sxs-lookup"><span data-stu-id="8b114-115">The following list shows the command-line switches that MDMERGE uses.</span></span>

<dl>

[<span data-ttu-id="8b114-116">**/i**</span><span class="sxs-lookup"><span data-stu-id="8b114-116">**/i**</span></span>](-mdmerge-i.md)  
[<span data-ttu-id="8b114-117">**/Metadata \_ dir**</span><span class="sxs-lookup"><span data-stu-id="8b114-117">**/metadata\_dir**</span></span>](-mdmerge-metadata-dir.md)  
[<span data-ttu-id="8b114-118">**/n**</span><span class="sxs-lookup"><span data-stu-id="8b114-118">**/n**</span></span>](-mdmerge-n.md)  
[<span data-ttu-id="8b114-119">**/o**</span><span class="sxs-lookup"><span data-stu-id="8b114-119">**/o**</span></span>](-mdmerge-o.md)  
[<span data-ttu-id="8b114-120">**/partial**</span><span class="sxs-lookup"><span data-stu-id="8b114-120">**/partial**</span></span>](-mdmerge-partial.md)  
[<span data-ttu-id="8b114-121">**/v**</span><span class="sxs-lookup"><span data-stu-id="8b114-121">**/v**</span></span>](-mdmerge-v.md)  
</dl>

<span data-ttu-id="8b114-122">Puede encontrar una lista completa de las opciones y los modificadores del compilador de MDMERGE cuando se usa la opción **-h** y **/?**</span><span class="sxs-lookup"><span data-stu-id="8b114-122">A complete listing of MDMERGE compiler switches and options is available when you use the **-h** and **/?**</span></span> <span data-ttu-id="8b114-123">centrales.</span><span class="sxs-lookup"><span data-stu-id="8b114-123">switches.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b114-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b114-124">Remarks</span></span>

<span data-ttu-id="8b114-125">La composición de metadatos permite que varios archivos IDL contengan definiciones para Windows Runtime componentes en el mismo espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="8b114-125">Metadata composition enables multiple IDL files to contain definitions for Windows Runtime components in the same namespace.</span></span> <span data-ttu-id="8b114-126">Esto le libera de definir todos los tipos en un espacio de nombres dentro de un solo archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="8b114-126">This frees you from defining all of the types in a namespace within a single IDL file.</span></span>

<span data-ttu-id="8b114-127">Es probable que tenga numerosos componentes de Windows Runtime que usan las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8b114-127">You're likely to have numerous Windows Runtime components that your apps use.</span></span> <span data-ttu-id="8b114-128">Cuando realice el paso final para generar ensamblados de metadatos de Windows Runtime que se pueden implementar, puede configurar MDMERGE para combinar componentes de varios directorios de metadatos, como los que se instalan con el sistema (% WINDOWS% \\ system32 \\ WinMetadata), los tipos de base y el directorio de compilación del proyecto actual.</span><span class="sxs-lookup"><span data-stu-id="8b114-128">When you perform the final step to produce deployable Windows Runtime metadata assemblies, you can configure MDMERGE to merge components from multiple metadata directories, like those that are installed with the system (%WINDOWS%\\system32\\WinMetadata), your foundation types, and your current project’s build directory.</span></span> <span data-ttu-id="8b114-129">Todos los tipos necesarios se combinan en los ensamblados de metadatos correctos e implementables que puede empaquetar para la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="8b114-129">All necessary types are merged into the correct, deployable, metadata assemblies that you can package for the Windows Store.</span></span>

<span data-ttu-id="8b114-130">Puede usar la opción [**/n**](-mdmerge-n.md) para especificar la profundidad de espacio de nombres admitida para la composición de ensamblados de metadatos.</span><span class="sxs-lookup"><span data-stu-id="8b114-130">You can use the [**/n**](-mdmerge-n.md) option to specify the supported namespace depth for composing metadata assemblies.</span></span> <span data-ttu-id="8b114-131">Esto permite configurar una división activa para los componentes de Windows Runtime, de modo que solo se empaqueta un archivo. winmd único en lugar de muchos.</span><span class="sxs-lookup"><span data-stu-id="8b114-131">This enables configuring a hot split for your Windows Runtime components, so that only a single .winmd file is packaged instead of many.</span></span> <span data-ttu-id="8b114-132">Esto reduce los tiempos de carga y e/s de archivo requeridos por las aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="8b114-132">This reduces the load times and file I/O required by your Windows Store apps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b114-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b114-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b114-134">Componentes de MIDLRT y Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="8b114-134">MIDLRT and Windows Runtime components</span></span>](midlrt-and-windows-runtime-components.md)
</dt> </dl>

 

 




