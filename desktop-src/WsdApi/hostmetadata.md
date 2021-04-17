---
description: Define los metadatos de hospedaje para el dispositivo que se va a implementar. Este elemento se usa solo para implementaciones de dispositivos (hosts).
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: elemento hostMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: becd6bc3eab6b1aa1d95414c6348288e0d29dbd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659975"
---
# <a name="hostmetadata-element"></a><span data-ttu-id="3887a-104">elemento hostMetadata</span><span class="sxs-lookup"><span data-stu-id="3887a-104">hostMetadata element</span></span>

<span data-ttu-id="3887a-105">Define los metadatos de hospedaje para el dispositivo que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="3887a-105">Defines the hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="3887a-106">Este elemento se usa solo para implementaciones de dispositivos (hosts).</span><span class="sxs-lookup"><span data-stu-id="3887a-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="3887a-107">Uso</span><span class="sxs-lookup"><span data-stu-id="3887a-107">Usage</span></span>

``` syntax
<hostMetadata>
  child elements
</hostMetadata>
```

## <a name="attributes"></a><span data-ttu-id="3887a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3887a-108">Attributes</span></span>

<span data-ttu-id="3887a-109">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="3887a-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3887a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3887a-110">Child elements</span></span>



| <span data-ttu-id="3887a-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="3887a-111">Element</span></span>                             | <span data-ttu-id="3887a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="3887a-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3887a-113">**organizar**</span><span class="sxs-lookup"><span data-stu-id="3887a-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="3887a-114">Define los elementos ServiceID y [**Types**](types.md) para el host de servicio.</span><span class="sxs-lookup"><span data-stu-id="3887a-114">Defines the ServiceID and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="3887a-115">Si no se proporciona explícitamente, WSDAPI no proporcionará datos predeterminados en respuesta a las solicitudes de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3887a-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                                          |
| [<span data-ttu-id="3887a-116">**ubicada**</span><span class="sxs-lookup"><span data-stu-id="3887a-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="3887a-117">Define los elementos [**ServiceID**](serviceid.md) y [**Types**](types.md) para los servicios proporcionados por este host de servicio.</span><span class="sxs-lookup"><span data-stu-id="3887a-117">Defines the [**ServiceID**](serviceid.md) and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="3887a-118">Cada servicio proporcionado por este host de servicio debe tener su propia información de elemento [**hospedado**](hosted.md) para asegurarse de que el servicio se publique correctamente en las respuestas a las solicitudes de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3887a-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="3887a-119">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3887a-119">Child element sequence</span></span>

``` syntax
(
  host?, 
  hosted+
)
```

## <a name="parent-elements"></a><span data-ttu-id="3887a-120">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="3887a-120">Parent elements</span></span>



| <span data-ttu-id="3887a-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="3887a-121">Element</span></span>                                                         | <span data-ttu-id="3887a-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="3887a-122">Description</span></span>                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="3887a-123">**relationshipMetadata**</span><span class="sxs-lookup"><span data-stu-id="3887a-123">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="3887a-124">Describe el host y los metadatos hospedados para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3887a-124">Describes the host and hosted metadata for the device.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="3887a-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3887a-125">Remarks</span></span>

<span data-ttu-id="3887a-126">Los metadatos de hospedaje aparecen en este elemento en un formato similar al especificado en el perfil de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3887a-126">The hosting metadata appears in this element in a form similar to the one specified in the device profile.</span></span> <span data-ttu-id="3887a-127">**hostMetadata** es ligeramente diferente del formato descrito en el perfil de dispositivo, ya que la única propiedad de referencia que admite es el identificador de servicio.</span><span class="sxs-lookup"><span data-stu-id="3887a-127">**hostMetadata** is slightly different from the format described in the device profile in that the only reference property it supports is the service ID.</span></span>

<span data-ttu-id="3887a-128">El elemento [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) se usa posteriormente para generar una constante de C que contiene esta información.</span><span class="sxs-lookup"><span data-stu-id="3887a-128">The [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) element is used subsequently to generate a C constant containing this information.</span></span>

## <a name="element-information"></a><span data-ttu-id="3887a-129">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="3887a-129">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="3887a-130">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3887a-130">Minimum supported system</span></span><br/> | <span data-ttu-id="3887a-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3887a-131">Windows Vista</span></span> |
| <span data-ttu-id="3887a-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3887a-132">Can be empty</span></span>                        | <span data-ttu-id="3887a-133">No</span><span class="sxs-lookup"><span data-stu-id="3887a-133">No</span></span>            |



 

 




