---
title: CPROPS. CPP
description: En el componente proveedor de ejemplo, se puede encontrar un ejemplo de una implementación de la caché de propiedades en cprops. cpp. En la tabla siguiente se enumeran los métodos admitidos.
ms.assetid: 51c9aa05-ca30-4d61-b3e3-d2f17a02b28f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b9f4fddfea6900fd8d7a06bee9979744eefd30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903068"
---
# <a name="cpropscpp"></a><span data-ttu-id="ba7b3-104">CPROPS. CPP</span><span class="sxs-lookup"><span data-stu-id="ba7b3-104">CPROPS.CPP</span></span>

<span data-ttu-id="ba7b3-105">En el componente proveedor de ejemplo, se puede encontrar un ejemplo de una implementación de la caché de propiedades en cprops. cpp.</span><span class="sxs-lookup"><span data-stu-id="ba7b3-105">In the example provider component, an example of a property cache implementation can be found in cprops.cpp.</span></span> <span data-ttu-id="ba7b3-106">En la tabla siguiente se enumeran los métodos admitidos.</span><span class="sxs-lookup"><span data-stu-id="ba7b3-106">Supported methods are listed in the following table.</span></span>



| <span data-ttu-id="ba7b3-107">Método</span><span class="sxs-lookup"><span data-stu-id="ba7b3-107">Method</span></span>                                           | <span data-ttu-id="ba7b3-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba7b3-108">Description</span></span>                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba7b3-109">**CPropertyCache:: AddProperty**</span><span class="sxs-lookup"><span data-stu-id="ba7b3-109">**CPropertyCache::addproperty**</span></span>                  | <span data-ttu-id="ba7b3-110">Amplíe la memoria caché de propiedades agregando una nueva.</span><span class="sxs-lookup"><span data-stu-id="ba7b3-110">Extend the property cache by adding a new one.</span></span>                                                                      |
| <span data-ttu-id="ba7b3-111">**CPropertyCache::updateproperty**</span><span class="sxs-lookup"><span data-stu-id="ba7b3-111">**CPropertyCache::updateproperty**</span></span>               | <span data-ttu-id="ba7b3-112">Buscar la propiedad, liberar su contenido y usar nuevos valores en su lugar. a continuación, marque la memoria caché modificada para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="ba7b3-112">Look up the property, free its contents, and use new values instead; then mark the cache changed for this property.</span></span> |
| <span data-ttu-id="ba7b3-113">**CPropertyCache::findproperty**</span><span class="sxs-lookup"><span data-stu-id="ba7b3-113">**CPropertyCache::findproperty**</span></span>                 | <span data-ttu-id="ba7b3-114">Buscar esta propiedad por su nombre; Guarde el índice.</span><span class="sxs-lookup"><span data-stu-id="ba7b3-114">Look up this property by name; save its index.</span></span>                                                                      |
| <span data-ttu-id="ba7b3-115">**CPropertyCache:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="ba7b3-115">**CPropertyCache::getproperty**</span></span>                  | <span data-ttu-id="ba7b3-116">Busque la propiedad en la memoria caché si está disponible; de lo contrario, llame a **GetInfo**.</span><span class="sxs-lookup"><span data-stu-id="ba7b3-116">Find the property in the cache if available, otherwise call **GetInfo**.</span></span> <span data-ttu-id="ba7b3-117">Establezca el índice y copie los nuevos valores.</span><span class="sxs-lookup"><span data-stu-id="ba7b3-117">Set the index and copy in the new values.</span></span>  |
| <span data-ttu-id="ba7b3-118">**CPropertyCache::p utproperty**</span><span class="sxs-lookup"><span data-stu-id="ba7b3-118">**CPropertyCache::putproperty**</span></span>                  | <span data-ttu-id="ba7b3-119">Busque la propiedad.</span><span class="sxs-lookup"><span data-stu-id="ba7b3-119">Find the property.</span></span> <span data-ttu-id="ba7b3-120">Libere lo que había y coloque los nuevos valores.</span><span class="sxs-lookup"><span data-stu-id="ba7b3-120">Free what was there and put in new values.</span></span>                                                       |
| <span data-ttu-id="ba7b3-121">**CPropertyCache::CPropertyCache**</span><span class="sxs-lookup"><span data-stu-id="ba7b3-121">**CPropertyCache::CPropertyCache**</span></span>               | <span data-ttu-id="ba7b3-122">Constructor estándar.</span><span class="sxs-lookup"><span data-stu-id="ba7b3-122">Standard constructor.</span></span>                                                                                               |
| <span data-ttu-id="ba7b3-123">**CPropertyCache:: ~ CPropertyCache**</span><span class="sxs-lookup"><span data-stu-id="ba7b3-123">**CPropertyCache::~CPropertyCache**</span></span>              | <span data-ttu-id="ba7b3-124">Destructor estándar.</span><span class="sxs-lookup"><span data-stu-id="ba7b3-124">Standard destructor.</span></span>                                                                                                |
| <span data-ttu-id="ba7b3-125">**CPropertyCache::createpropertycache**</span><span class="sxs-lookup"><span data-stu-id="ba7b3-125">**CPropertyCache::createpropertycache**</span></span>          | <span data-ttu-id="ba7b3-126">Cree la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="ba7b3-126">Create the cache.</span></span>                                                                                                   |
| <span data-ttu-id="ba7b3-127">**CPropertyCache::unboundgetproperty**</span><span class="sxs-lookup"><span data-stu-id="ba7b3-127">**CPropertyCache::unboundgetproperty**</span></span>           | <span data-ttu-id="ba7b3-128">Busque la propiedad en la memoria caché y establézcala en estos valores.</span><span class="sxs-lookup"><span data-stu-id="ba7b3-128">Find the property in the cache and set it to these values.</span></span>                                                          |
| <span data-ttu-id="ba7b3-129">**CPropertyCache::SampleDSMarshallProperties**</span><span class="sxs-lookup"><span data-stu-id="ba7b3-129">**CPropertyCache::SampleDSMarshallProperties**</span></span>   | <span data-ttu-id="ba7b3-130">Calcula las referencias de los datos y los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ba7b3-130">Marshal property data and values.</span></span>                                                                                   |
| <span data-ttu-id="ba7b3-131">**CPropertyCache::marshallproperty**</span><span class="sxs-lookup"><span data-stu-id="ba7b3-131">**CPropertyCache::marshallproperty**</span></span>             | <span data-ttu-id="ba7b3-132">Calcular las referencias de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="ba7b3-132">Marshal a property.</span></span>                                                                                                 |
| <span data-ttu-id="ba7b3-133">**CPropertyCache::SampleDSUnMarshallProperties**</span><span class="sxs-lookup"><span data-stu-id="ba7b3-133">**CPropertyCache::SampleDSUnMarshallProperties**</span></span> | <span data-ttu-id="ba7b3-134">Anular la serialización de los datos y valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ba7b3-134">Unmarshal property data and values.</span></span>                                                                                 |
| <span data-ttu-id="ba7b3-135">**CPropertyCache::unmarshallproperty**</span><span class="sxs-lookup"><span data-stu-id="ba7b3-135">**CPropertyCache::unmarshallproperty**</span></span>           | <span data-ttu-id="ba7b3-136">Desserialización de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="ba7b3-136">Unmarshal a property.</span></span>                                                                                               |



 

 

 




