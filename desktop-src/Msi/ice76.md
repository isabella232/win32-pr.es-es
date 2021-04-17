---
description: ICE76 comprueba el uso del catálogo SFP (WFP) dentro de Windows Installer paquetes para Windows me. Esta ICE también comprueba que ningún archivo de la tabla BindImage hace referencia a los catálogos SFP.
ms.assetid: e8b60b11-19ac-4ec4-aa36-a1f7a3ccd6f6
title: ICE76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5beb0157053e9bd3e4bf0d896f52af04a511ac24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652466"
---
# <a name="ice76"></a><span data-ttu-id="930f6-104">ICE76</span><span class="sxs-lookup"><span data-stu-id="930f6-104">ICE76</span></span>

<span data-ttu-id="930f6-105">ICE76 comprueba el uso del catálogo SFP (WFP) dentro de Windows Installer paquetes para Windows me.</span><span class="sxs-lookup"><span data-stu-id="930f6-105">ICE76 verifies the use of the SFP (WFP) catalog within Windows Installer packages for Windows Me.</span></span> <span data-ttu-id="930f6-106">Esta ICE también comprueba que ningún archivo de la [tabla](bindimage-table.md) BindImage hace referencia a los catálogos SFP.</span><span class="sxs-lookup"><span data-stu-id="930f6-106">This ICE also verifies that no files in the BindImage [table](bindimage-table.md) reference SFP catalogs.</span></span>

<span data-ttu-id="930f6-107">La protección de archivos de Windows requiere una coincidencia exacta entre el archivo y la firma incrustada en el archivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="930f6-107">Windows File Protection requires an exact match between the file and the signature embedded in the catalog file.</span></span> <span data-ttu-id="930f6-108">Los archivos que hacen referencia a un catálogo SFP no deben aparecer en la tabla BindImage porque el efecto de la [acción BindImage](bindimage-action.md) en estos archivos difiere entre los equipos.</span><span class="sxs-lookup"><span data-stu-id="930f6-108">Files that reference a SFP catalog must not be listed in the BindImage table because the effect of the [BindImage action](bindimage-action.md) on these files differs between computers.</span></span> <span data-ttu-id="930f6-109">Los archivos a los que hacen referencia los catálogos SFP deben encontrarse en componentes permanentes o instalados localmente.</span><span class="sxs-lookup"><span data-stu-id="930f6-109">Files referenced by SFP catalogs must be in components that are permanent or installed locally.</span></span>

## <a name="result"></a><span data-ttu-id="930f6-110">Resultado</span><span class="sxs-lookup"><span data-stu-id="930f6-110">Result</span></span>

<span data-ttu-id="930f6-111">ICE76 publica un error para cada archivo de la [tabla BindImage](bindimage-table.md) que también está en la [tabla FileSFPCatalog](filesfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="930f6-111">ICE76 posts an error for each file in the [BindImage table](bindimage-table.md) that is also in the [FileSFPCatalog table](filesfpcatalog-table.md).</span></span>

<span data-ttu-id="930f6-112">ICE76 genera un error si un archivo de la tabla FileSFPCatalog pertenece a un componente con cualquiera de los siguientes elementos true:</span><span class="sxs-lookup"><span data-stu-id="930f6-112">ICE76 outputs an error if a file in the FileSFPCatalog table belongs to a component with any of the following true:</span></span>

-   <span data-ttu-id="930f6-113">**msidbComponentAttributesPermanent** no se establece en la columna Attributes de la [tabla Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="930f6-113">**msidbComponentAttributesPermanent** is not set in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="930f6-114">**msidbComponentAttributesSourceOnly** se establece en la columna Attributes de la tabla Component.</span><span class="sxs-lookup"><span data-stu-id="930f6-114">**msidbComponentAttributesSourceOnly** is set in the Attributes column of the Component table.</span></span>
-   <span data-ttu-id="930f6-115">**msidbAttributesOptional** se establece en la columna Attributes de la tabla Component.</span><span class="sxs-lookup"><span data-stu-id="930f6-115">**msidbAttributesOptional** is set in the Attributes column of the Component table.</span></span>

## <a name="example"></a><span data-ttu-id="930f6-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="930f6-116">Example</span></span>

<span data-ttu-id="930f6-117">ICE76 notifica el siguiente error para el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="930f6-117">ICE76 reports the following error for the example:</span></span>

``` syntax
File 'File1' references a SFP catalog. Therefore it cannot be in the BindImage table.
```

<span data-ttu-id="930f6-118">[Tabla FileSFPCatalog](filesfpcatalog-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="930f6-118">[FileSFPCatalog Table](filesfpcatalog-table.md) (partial)</span></span>



| <span data-ttu-id="930f6-119">Archivo\_</span><span class="sxs-lookup"><span data-stu-id="930f6-119">File\_</span></span> | <span data-ttu-id="930f6-120">SFPCatalog\_</span><span class="sxs-lookup"><span data-stu-id="930f6-120">SFPCatalog\_</span></span> |
|--------|--------------|
| <span data-ttu-id="930f6-121">Archivo1</span><span class="sxs-lookup"><span data-stu-id="930f6-121">File1</span></span>  | <span data-ttu-id="930f6-122">Catalog1.Cat</span><span class="sxs-lookup"><span data-stu-id="930f6-122">Catalog1.Cat</span></span> |



 

<span data-ttu-id="930f6-123">[Tabla BindImage](bindimage-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="930f6-123">[BindImage Table](bindimage-table.md) (partial)</span></span>



| <span data-ttu-id="930f6-124">Archivo\_</span><span class="sxs-lookup"><span data-stu-id="930f6-124">File\_</span></span> |
|--------|
| <span data-ttu-id="930f6-125">Archivo1</span><span class="sxs-lookup"><span data-stu-id="930f6-125">File1</span></span>  |



 

<span data-ttu-id="930f6-126">Para corregir esto, no escriba ningún archivo que haga referencia a los catálogos de SFP en la tabla BindImage.</span><span class="sxs-lookup"><span data-stu-id="930f6-126">To fix this do not enter any files that reference SFP catalogs into the BindImage table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="930f6-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="930f6-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="930f6-128">Tabla BindImage</span><span class="sxs-lookup"><span data-stu-id="930f6-128">BindImage Table</span></span>](bindimage-table.md)
</dt> <dt>

[<span data-ttu-id="930f6-129">Tabla de componentes</span><span class="sxs-lookup"><span data-stu-id="930f6-129">Component Table</span></span>](component-table.md)
</dt> <dt>

[<span data-ttu-id="930f6-130">Tabla FileSFPCatalog</span><span class="sxs-lookup"><span data-stu-id="930f6-130">FileSFPCatalog Table</span></span>](filesfpcatalog-table.md)
</dt> <dt>

[<span data-ttu-id="930f6-131">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="930f6-131">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



