---
description: Representa una colección de objetos de extensión.
ms.assetid: b0d69df9-12c4-4872-b883-b029c4350502
title: Objeto NoticeNumbers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 58d954fdeef66d6d0e5eadb3086cb549b59e5669
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690832"
---
# <a name="noticenumbers-object"></a><span data-ttu-id="b6a71-103">Objeto NoticeNumbers</span><span class="sxs-lookup"><span data-stu-id="b6a71-103">NoticeNumbers object</span></span>

<span data-ttu-id="b6a71-104">\[El objeto **NoticeNumbers** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="b6a71-104">\[The **NoticeNumbers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b6a71-105">Para obtener más información, vea [**calificador**](qualifier.md).\]</span><span class="sxs-lookup"><span data-stu-id="b6a71-105">For more information, see [**Qualifier**](qualifier.md).\]</span></span>

<span data-ttu-id="b6a71-106">El objeto **NoticeNumbers** representa una colección de objetos de [**extensión**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="b6a71-106">The **NoticeNumbers** object represents a collection of [**Extension**](extension.md) objects.</span></span> <span data-ttu-id="b6a71-107">Cada objeto de [**extensión**](extension.md) representa un número de aviso de usuario.</span><span class="sxs-lookup"><span data-stu-id="b6a71-107">Each [**Extension**](extension.md) object represents a user notice number.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="b6a71-108">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="b6a71-108">When to use</span></span>

<span data-ttu-id="b6a71-109">El objeto **NoticeNumbers** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="b6a71-109">The **NoticeNumbers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="b6a71-110">Recupera el número de objetos de [**extensión**](extension.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="b6a71-110">Retrieve the number of [**Extension**](extension.md) objects in the collection.</span></span>
-   <span data-ttu-id="b6a71-111">Recupera un objeto de [**extensión**](extension.md) específico de la colección.</span><span class="sxs-lookup"><span data-stu-id="b6a71-111">Retrieve a specific [**Extension**](extension.md) object from the collection.</span></span>
-   <span data-ttu-id="b6a71-112">Recorrer en iteración la colección.</span><span class="sxs-lookup"><span data-stu-id="b6a71-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="b6a71-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="b6a71-113">Members</span></span>

<span data-ttu-id="b6a71-114">El objeto **NoticeNumbers** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b6a71-114">The **NoticeNumbers** object has these types of members:</span></span>

-   [<span data-ttu-id="b6a71-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b6a71-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6a71-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b6a71-116">Properties</span></span>

<span data-ttu-id="b6a71-117">El objeto **NoticeNumbers** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b6a71-117">The **NoticeNumbers** object has these properties.</span></span>



| <span data-ttu-id="b6a71-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b6a71-118">Property</span></span>                                              | <span data-ttu-id="b6a71-119">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="b6a71-119">Access type</span></span>          | <span data-ttu-id="b6a71-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6a71-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6a71-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="b6a71-121">**\_NewEnum**</span></span>](noticenumbers-newenum.md)<br/> | <span data-ttu-id="b6a71-122">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6a71-122">Read-only</span></span><br/> | <span data-ttu-id="b6a71-123">Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="b6a71-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="b6a71-124">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="b6a71-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="b6a71-125">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="b6a71-125">**Count**</span></span>](noticenumbers-count.md)<br/>       | <span data-ttu-id="b6a71-126">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6a71-126">Read-only</span></span><br/> | <span data-ttu-id="b6a71-127">Recupera el número de objetos de [**extensión**](extension.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="b6a71-127">Retrieves the number of [**Extension**](extension.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="b6a71-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b6a71-128">**Item**</span></span>](noticenumbers-item.md)<br/>         | <span data-ttu-id="b6a71-129">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6a71-129">Read-only</span></span><br/> | <span data-ttu-id="b6a71-130">Recupera el objeto de [**extensión**](extension.md) que representa el número de aviso indizado de la colección.</span><span class="sxs-lookup"><span data-stu-id="b6a71-130">Retrieves the [**Extension**](extension.md) object that represents the indexed notice number of the collection.</span></span><br/> <span data-ttu-id="b6a71-131">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b6a71-131">This is the default property.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="b6a71-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6a71-132">Remarks</span></span>

<span data-ttu-id="b6a71-133">No se puede crear el objeto **NoticeNumbers** .</span><span class="sxs-lookup"><span data-stu-id="b6a71-133">The **NoticeNumbers** object cannot be created.</span></span>

<span data-ttu-id="b6a71-134">El objeto NoticeNumbers se usa en la propiedad [**Qualifier. NoticeNumbers**](qualifier-noticenumbers.md) .</span><span class="sxs-lookup"><span data-stu-id="b6a71-134">The NoticeNumbers object is used in the [**Qualifier.NoticeNumbers**](qualifier-noticenumbers.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6a71-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6a71-135">Requirements</span></span>



| <span data-ttu-id="b6a71-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6a71-136">Requirement</span></span> | <span data-ttu-id="b6a71-137">Value</span><span class="sxs-lookup"><span data-stu-id="b6a71-137">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6a71-138">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b6a71-138">Redistributable</span></span><br/> | <span data-ttu-id="b6a71-139">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="b6a71-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b6a71-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b6a71-140">DLL</span></span><br/>             | <dl> <span data-ttu-id="b6a71-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6a71-141"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
