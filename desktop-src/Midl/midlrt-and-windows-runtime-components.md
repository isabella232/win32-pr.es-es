---
title: Componentes de MIDLRT y Windows Runtime
description: Muestra cómo crear archivos de metadatos (. winmd) que representan la API de los componentes de Windows Runtime personalizados.
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- MIDL del compilador MIDL
- MIDL del compilador MIDL, MIDL y Windows Runtime winrt
- Windows Runtime MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edf4d40b3fc5b0a5ed8eeb9b5fd47a3b87c4543
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104533603"
---
# <a name="midlrt-and-windows-runtime-components"></a><span data-ttu-id="7d7b3-106">Componentes de MIDLRT y Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="7d7b3-106">MIDLRT and Windows Runtime components</span></span>

<span data-ttu-id="7d7b3-107">Muestra cómo crear archivos de metadatos (. winmd) que representan la API de los componentes de Windows Runtime personalizados.</span><span class="sxs-lookup"><span data-stu-id="7d7b3-107">Shows how to create metadata (.winmd) files that represent the API for custom Windows Runtime components.</span></span>


<span data-ttu-id="7d7b3-108">Use el compilador MIDLRT para compilar archivos de metadatos (. winmd) para los componentes de Windows Runtime personalizados.</span><span class="sxs-lookup"><span data-stu-id="7d7b3-108">Use the MIDLRT compiler to build metadata (.winmd) files for your custom Windows Runtime components.</span></span>

<span data-ttu-id="7d7b3-109">Cuando se generan los archivos de metadatos, puede crearlos en un paquete más eficaz mediante la utilidad MDMERGE.</span><span class="sxs-lookup"><span data-stu-id="7d7b3-109">When your metadata files are generated, you can compose them into a more efficient package by using the MDMERGE utility.</span></span> <span data-ttu-id="7d7b3-110">Para obtener más información, vea [MDMERGE and Metadata files](mdmerge-and-metadata-files.md).</span><span class="sxs-lookup"><span data-stu-id="7d7b3-110">For more info, see [MDMERGE and metadata files](mdmerge-and-metadata-files.md).</span></span>


<span data-ttu-id="7d7b3-111">El uso de MIDLRT es similar al uso del compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="7d7b3-111">Using MIDLRT is similar to using the MIDL compiler.</span></span> <span data-ttu-id="7d7b3-112">Ejecute MIDLRT desde la línea de comandos con el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="7d7b3-112">Run MIDLRT from the command line using the following command:</span></span>

<span data-ttu-id="7d7b3-113">**midlrt**  *<* **Opciones** _>_ de **nombre de archivo. idl**</span><span class="sxs-lookup"><span data-stu-id="7d7b3-113">**midlrt** \*<\***options**_>_ **filename.idl**</span></span>

<span data-ttu-id="7d7b3-114">donde \*\*\* < \*\*\* _>_ representa las opciones de línea de comandos que quiere usar y FILENAME. idl es el nombre del archivo IDL que se va a compilar.</span><span class="sxs-lookup"><span data-stu-id="7d7b3-114">where \*<\***options**_>_ represents the command-line options you want to use, and Filename.idl is the name of the IDL file to compile.</span></span>


<span data-ttu-id="7d7b3-115">En la lista siguiente se muestran los modificadores de la línea de comandos que usa MIDLRT.EXE.</span><span class="sxs-lookup"><span data-stu-id="7d7b3-115">The following list shows the command-line switches that MIDLRT.EXE uses.</span></span>

<dl>

[<span data-ttu-id="7d7b3-116">**/enum ( \_ clase)**</span><span class="sxs-lookup"><span data-stu-id="7d7b3-116">**/enum\_class**</span></span>](-enum-class.md)  
[<span data-ttu-id="7d7b3-117">**/Metadata \_ dir**</span><span class="sxs-lookup"><span data-stu-id="7d7b3-117">**/metadata\_dir**</span></span>](-metadata-dir.md)  
[<span data-ttu-id="7d7b3-118">**/nomidl**</span><span class="sxs-lookup"><span data-stu-id="7d7b3-118">**/nomidl**</span></span>](-nomidl.md)  
[<span data-ttu-id="7d7b3-119">**/nomd**</span><span class="sxs-lookup"><span data-stu-id="7d7b3-119">**/nomd**</span></span>](-nomd.md)  
[<span data-ttu-id="7d7b3-120">**/NS ( \_ prefijo)**</span><span class="sxs-lookup"><span data-stu-id="7d7b3-120">**/ns\_prefix**</span></span>](-ns-prefix.md)  
[<span data-ttu-id="7d7b3-121">**/winmd**</span><span class="sxs-lookup"><span data-stu-id="7d7b3-121">**/winmd**</span></span>](-winmd.md)  
[<span data-ttu-id="7d7b3-122">**/winrt**</span><span class="sxs-lookup"><span data-stu-id="7d7b3-122">**/winrt**</span></span>](-winrt.md)  
</dl>

<span data-ttu-id="7d7b3-123">Puede encontrar una lista completa de las opciones y los modificadores del compilador de MIDLRT cuando se usa el compilador MIDLRT [**/Help**](-help-.md) y/?</span><span class="sxs-lookup"><span data-stu-id="7d7b3-123">A complete listing of MIDLRT compiler switches and options is available when you use the MIDLRT compiler [**/help**](-help-.md) and /?</span></span> <span data-ttu-id="7d7b3-124">centrales.</span><span class="sxs-lookup"><span data-stu-id="7d7b3-124">switches.</span></span> <span data-ttu-id="7d7b3-125">Los modificadores están organizados por categorías.</span><span class="sxs-lookup"><span data-stu-id="7d7b3-125">The switches are organized by categories.</span></span> <span data-ttu-id="7d7b3-126">Para obtener más información, vea la [referencia de Command-Line de MIDL](midl-command-line-reference.md).</span><span class="sxs-lookup"><span data-stu-id="7d7b3-126">For more info, see the [MIDL Command-Line Reference](midl-command-line-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d7b3-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7d7b3-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d7b3-128">Archivos de metadatos y MDMERGE</span><span class="sxs-lookup"><span data-stu-id="7d7b3-128">MDMERGE and metadata files</span></span>](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




