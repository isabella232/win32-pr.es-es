---
title: Asignación de código ADSI Visual Basic a código de C++
description: ADSI consta de más de 50 interfaces.
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c64a022569a95f38ec1da7a1cb7acf533eb04ca6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656164"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a><span data-ttu-id="b0c8d-103">Asignación de código ADSI Visual Basic a código de C++</span><span class="sxs-lookup"><span data-stu-id="b0c8d-103">Mapping ADSI Visual Basic Code to C++ Code</span></span>

<span data-ttu-id="b0c8d-104">ADSI consta de más de 50 interfaces.</span><span class="sxs-lookup"><span data-stu-id="b0c8d-104">ADSI consists of more than 50 interfaces.</span></span> <span data-ttu-id="b0c8d-105">La mayoría de las operaciones de directorio se pueden completar con solo cinco interfaces.</span><span class="sxs-lookup"><span data-stu-id="b0c8d-105">Most directory operations can be completed using only five interfaces.</span></span> <span data-ttu-id="b0c8d-106">Son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="b0c8d-106">They are:</span></span>

-   [<span data-ttu-id="b0c8d-107">**IADsOpenDSObject**</span><span class="sxs-lookup"><span data-stu-id="b0c8d-107">**IADsOpenDSObject**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)
-   [<span data-ttu-id="b0c8d-108">**IADs**</span><span class="sxs-lookup"><span data-stu-id="b0c8d-108">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
-   [<span data-ttu-id="b0c8d-109">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="b0c8d-109">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [<span data-ttu-id="b0c8d-110">**IDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="b0c8d-110">**IDirectoryObject**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [<span data-ttu-id="b0c8d-111">**IDirectorySearch**</span><span class="sxs-lookup"><span data-stu-id="b0c8d-111">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

<span data-ttu-id="b0c8d-112">En la tabla siguiente se enumeran las asignaciones de código ADSI VB/VBS a código de C++.</span><span class="sxs-lookup"><span data-stu-id="b0c8d-112">The following table lists mappings from ADSI VB/VBS code to C++ code.</span></span> <span data-ttu-id="b0c8d-113">Tenga en cuenta que esta no es una lista completa.</span><span class="sxs-lookup"><span data-stu-id="b0c8d-113">Be aware that this is not a complete list.</span></span>



| <span data-ttu-id="b0c8d-114">Código VBS</span><span class="sxs-lookup"><span data-stu-id="b0c8d-114">VBS Code</span></span>                           | <span data-ttu-id="b0c8d-115">Código VC</span><span class="sxs-lookup"><span data-stu-id="b0c8d-115">VC Code</span></span>                                                               |
|------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="b0c8d-116">Set obj = GetObject ()</span><span class="sxs-lookup"><span data-stu-id="b0c8d-116">Set obj = GetObject()</span></span>              | <span data-ttu-id="b0c8d-117">HR = AdsGetObject ()</span><span class="sxs-lookup"><span data-stu-id="b0c8d-117">hr = AdsGetObject()</span></span>                                                   |
| <span data-ttu-id="b0c8d-118">obj. Put obj. Obtener obj. Aérea</span><span class="sxs-lookup"><span data-stu-id="b0c8d-118">obj.Put obj.Get obj.Parent</span></span>         | <span data-ttu-id="b0c8d-119">IADs o IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="b0c8d-119">IADs or IDirectoryObject</span></span>                                              |
| <span data-ttu-id="b0c8d-120">obj. Crear obj. Eliminar obj. MoveHere</span><span class="sxs-lookup"><span data-stu-id="b0c8d-120">obj.Create obj.Delete obj.MoveHere</span></span> | <span data-ttu-id="b0c8d-121">IADsContainer</span><span class="sxs-lookup"><span data-stu-id="b0c8d-121">IADsContainer</span></span>                                                         |
| <span data-ttu-id="b0c8d-122">Para cada...</span><span class="sxs-lookup"><span data-stu-id="b0c8d-122">For each…</span></span> <span data-ttu-id="b0c8d-123">en...</span><span class="sxs-lookup"><span data-stu-id="b0c8d-123">in…</span></span>                      | <span data-ttu-id="b0c8d-124">AdsBuildEnumerator() ADsEnumerateNext()</span><span class="sxs-lookup"><span data-stu-id="b0c8d-124">AdsBuildEnumerator() ADsEnumerateNext()</span></span>                               |
| <span data-ttu-id="b0c8d-125">Conexión, comando, conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="b0c8d-125">Connection, Command, RecordSet</span></span>     | <span data-ttu-id="b0c8d-126">IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="b0c8d-126">IDirectorySearch</span></span>                                                      |
| <span data-ttu-id="b0c8d-127">Descriptor de seguridad, ACL, ACE</span><span class="sxs-lookup"><span data-stu-id="b0c8d-127">Security descriptor, ACL, ACE</span></span>      | <span data-ttu-id="b0c8d-128">IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="b0c8d-128">IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry</span></span> |



 

 

 




