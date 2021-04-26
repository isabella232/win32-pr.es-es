---
description: Define los metadatos de hospedaje para el dispositivo que se va a implementar. Este elemento solo se usa para implementaciones de dispositivos (hosts).
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: hostMetadata, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9cf6fa139a2723ed90dfe281fc7b054016386fa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994802"
---
# <a name="hostmetadata-element"></a><span data-ttu-id="c60dc-104">hostMetadata, elemento</span><span class="sxs-lookup"><span data-stu-id="c60dc-104">hostMetadata element</span></span>

<span data-ttu-id="c60dc-105">Define los metadatos de hospedaje para el dispositivo que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="c60dc-105">Defines the hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="c60dc-106">Este elemento solo se usa para implementaciones de dispositivos (hosts).</span><span class="sxs-lookup"><span data-stu-id="c60dc-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="c60dc-107">Uso</span><span class="sxs-lookup"><span data-stu-id="c60dc-107">Usage</span></span>

``` syntax
<hostMetadata>
  child elements
</hostMetadata>
```

## <a name="attributes"></a><span data-ttu-id="c60dc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c60dc-108">Attributes</span></span>

<span data-ttu-id="c60dc-109">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="c60dc-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c60dc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c60dc-110">Child elements</span></span>



| <span data-ttu-id="c60dc-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="c60dc-111">Element</span></span>                             | <span data-ttu-id="c60dc-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c60dc-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c60dc-113">**Host**</span><span class="sxs-lookup"><span data-stu-id="c60dc-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="c60dc-114">Define los elementos ServiceID y [**Types**](types.md) para el host de servicio.</span><span class="sxs-lookup"><span data-stu-id="c60dc-114">Defines the ServiceID and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="c60dc-115">Si no se proporciona explícitamente, WSDAPI no suministrará ningún dato predeterminado en respuesta a las solicitudes de metadatos.</span><span class="sxs-lookup"><span data-stu-id="c60dc-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                                          |
| [<span data-ttu-id="c60dc-116">**Alojados**</span><span class="sxs-lookup"><span data-stu-id="c60dc-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="c60dc-117">Define los [**elementos ServiceID**](serviceid.md) y [**Types**](types.md) para los servicios proporcionados por este host de servicio.</span><span class="sxs-lookup"><span data-stu-id="c60dc-117">Defines the [**ServiceID**](serviceid.md) and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="c60dc-118">Cada servicio proporcionado por este host [](hosted.md) de servicio debe tener su propia información de elemento hospedado para asegurarse de que el servicio se publica correctamente en respuestas a solicitudes de metadatos.</span><span class="sxs-lookup"><span data-stu-id="c60dc-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="c60dc-119">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c60dc-119">Child element sequence</span></span>

``` syntax
(
  host?, 
  hosted+
)
```

## <a name="parent-elements"></a><span data-ttu-id="c60dc-120">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="c60dc-120">Parent elements</span></span>



| <span data-ttu-id="c60dc-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="c60dc-121">Element</span></span>                                                         | <span data-ttu-id="c60dc-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="c60dc-122">Description</span></span>                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="c60dc-123">**relationshipMetadata**</span><span class="sxs-lookup"><span data-stu-id="c60dc-123">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="c60dc-124">Describe el host y los metadatos hospedados para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c60dc-124">Describes the host and hosted metadata for the device.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="c60dc-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c60dc-125">Remarks</span></span>

<span data-ttu-id="c60dc-126">Los metadatos de hospedaje aparecen en este elemento con un formato similar al especificado en el perfil de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c60dc-126">The hosting metadata appears in this element in a form similar to the one specified in the device profile.</span></span> <span data-ttu-id="c60dc-127">**hostMetadata es** ligeramente diferente del formato descrito en el perfil de dispositivo en que la única propiedad de referencia que admite es el identificador de servicio.</span><span class="sxs-lookup"><span data-stu-id="c60dc-127">**hostMetadata** is slightly different from the format described in the device profile in that the only reference property it supports is the service ID.</span></span>

<span data-ttu-id="c60dc-128">El [**elemento relationshipMetadataDefinition**](relationshipmetadatadefinition.md) se usa posteriormente para generar una constante de C que contiene esta información.</span><span class="sxs-lookup"><span data-stu-id="c60dc-128">The [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) element is used subsequently to generate a C constant containing this information.</span></span>

## <a name="element-information"></a><span data-ttu-id="c60dc-129">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="c60dc-129">Element information</span></span>



| <span data-ttu-id="c60dc-130">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="c60dc-130">Label</span></span> | <span data-ttu-id="c60dc-131">Value</span><span class="sxs-lookup"><span data-stu-id="c60dc-131">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="c60dc-132">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c60dc-132">Minimum supported system</span></span><br/> | <span data-ttu-id="c60dc-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c60dc-133">Windows Vista</span></span> |
| <span data-ttu-id="c60dc-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c60dc-134">Can be empty</span></span>                        | <span data-ttu-id="c60dc-135">No</span><span class="sxs-lookup"><span data-stu-id="c60dc-135">No</span></span>            |



 

 




