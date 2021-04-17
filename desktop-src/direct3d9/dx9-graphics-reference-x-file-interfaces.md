---
description: Esta sección contiene información de referencia de las interfaces COM que se usan para leer y escribir desde archivos de DirectX. x. En desuso.
ms.assetid: 66e3476a-4ee8-48ac-aab8-6653793e0ef3
title: Interfaces de archivo X
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6e47325a4912faeb919cb60571de3cccbbe265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537605"
---
# <a name="x-file-interfaces"></a><span data-ttu-id="45100-104">Interfaces de archivo X</span><span class="sxs-lookup"><span data-stu-id="45100-104">X File Interfaces</span></span>

<span data-ttu-id="45100-105">Esta sección contiene información de referencia de las interfaces COM que se usan para leer y escribir desde archivos de DirectX. x.</span><span class="sxs-lookup"><span data-stu-id="45100-105">This section contains reference information for the COM interfaces used to read to and write from DirectX .x files.</span></span> <span data-ttu-id="45100-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="45100-106">Deprecated.</span></span>

-   [<span data-ttu-id="45100-107">**IDirectXFile**</span><span class="sxs-lookup"><span data-stu-id="45100-107">**IDirectXFile**</span></span>](idirectxfile.md)
-   [<span data-ttu-id="45100-108">**IDirectXFileBinary**</span><span class="sxs-lookup"><span data-stu-id="45100-108">**IDirectXFileBinary**</span></span>](idirectxfilebinary.md)
-   [<span data-ttu-id="45100-109">**IDirectXFileData**</span><span class="sxs-lookup"><span data-stu-id="45100-109">**IDirectXFileData**</span></span>](idirectxfiledata.md)
-   [<span data-ttu-id="45100-110">**IDirectXFileDataReference**</span><span class="sxs-lookup"><span data-stu-id="45100-110">**IDirectXFileDataReference**</span></span>](idirectxfiledatareference.md)
-   [<span data-ttu-id="45100-111">**IDirectXFileEnumObject**</span><span class="sxs-lookup"><span data-stu-id="45100-111">**IDirectXFileEnumObject**</span></span>](idirectxfileenumobject.md)
-   [<span data-ttu-id="45100-112">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="45100-112">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
-   [<span data-ttu-id="45100-113">**IDirectXFileSaveObject**</span><span class="sxs-lookup"><span data-stu-id="45100-113">**IDirectXFileSaveObject**</span></span>](idirectxfilesaveobject.md)

<span data-ttu-id="45100-114">En las tablas siguientes se muestra la relación entre las interfaces de archivo. x.</span><span class="sxs-lookup"><span data-stu-id="45100-114">The following tables illustrate the relationship between the .x file interfaces.</span></span>



| <span data-ttu-id="45100-115">Interfaz</span><span class="sxs-lookup"><span data-stu-id="45100-115">Interface</span></span>             | <span data-ttu-id="45100-116">Deriva de</span><span class="sxs-lookup"><span data-stu-id="45100-116">Derives from</span></span>           | <span data-ttu-id="45100-117">Deriva de</span><span class="sxs-lookup"><span data-stu-id="45100-117">Derives from</span></span> |
|-----------------------|------------------------|--------------|
|                       | <span data-ttu-id="45100-118">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="45100-118">IDirectXFile</span></span>           | <span data-ttu-id="45100-119">IUnknown</span><span class="sxs-lookup"><span data-stu-id="45100-119">IUnknown</span></span>     |
| <span data-ttu-id="45100-120">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="45100-120">IDirectXFileBinary</span></span>    | <span data-ttu-id="45100-121">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="45100-121">IDirectXFileObject</span></span>     | <span data-ttu-id="45100-122">IUnknown</span><span class="sxs-lookup"><span data-stu-id="45100-122">IUnknown</span></span>     |
| <span data-ttu-id="45100-123">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="45100-123">IDirectXFileData</span></span>      | <span data-ttu-id="45100-124">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="45100-124">IDirectXFileObject</span></span>     | <span data-ttu-id="45100-125">IUnknown</span><span class="sxs-lookup"><span data-stu-id="45100-125">IUnknown</span></span>     |
| <span data-ttu-id="45100-126">IDirectXFileReference</span><span class="sxs-lookup"><span data-stu-id="45100-126">IDirectXFileReference</span></span> | <span data-ttu-id="45100-127">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="45100-127">IDirectXFileObject</span></span>     | <span data-ttu-id="45100-128">IUnknown</span><span class="sxs-lookup"><span data-stu-id="45100-128">IUnknown</span></span>     |
|                       | <span data-ttu-id="45100-129">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="45100-129">IDirectXFileSaveObject</span></span> | <span data-ttu-id="45100-130">IUnknown</span><span class="sxs-lookup"><span data-stu-id="45100-130">IUnknown</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="45100-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="45100-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45100-132">Referencia de archivo X (heredado)</span><span class="sxs-lookup"><span data-stu-id="45100-132">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



