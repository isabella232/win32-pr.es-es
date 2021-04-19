---
description: Define los elementos ServiceID, Types, PnPXHardwareId y PnPXCompatibleId para los servicios definidos por el host de servicio.
ms.assetid: f901a88f-7e01-4e7f-a0f2-59f2a01b03cd
title: elemento hospedado
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d46549898f0a95de362467c759c3d95eb806a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706975"
---
# <a name="hosted-element"></a><span data-ttu-id="132a8-103">elemento hospedado</span><span class="sxs-lookup"><span data-stu-id="132a8-103">hosted element</span></span>

<span data-ttu-id="132a8-104">Define los elementos [**ServiceID**](serviceid.md), [**Types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md)y [**PnPXCompatibleId**](pnpxcompatibleid.md) para los servicios definidos por el host de servicio.</span><span class="sxs-lookup"><span data-stu-id="132a8-104">Defines the [**ServiceID**](serviceid.md), [**Types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md), and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements for the services defined by the service host.</span></span>

## <a name="usage"></a><span data-ttu-id="132a8-105">Uso</span><span class="sxs-lookup"><span data-stu-id="132a8-105">Usage</span></span>

``` syntax
<hosted>
  child elements
</hosted>
```

## <a name="attributes"></a><span data-ttu-id="132a8-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="132a8-106">Attributes</span></span>

<span data-ttu-id="132a8-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="132a8-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="132a8-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="132a8-108">Child elements</span></span>



| <span data-ttu-id="132a8-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="132a8-109">Element</span></span>                                                 | <span data-ttu-id="132a8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="132a8-110">Description</span></span>                                                                      |
|---------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="132a8-111">**PnPXCompatibleId**</span><span class="sxs-lookup"><span data-stu-id="132a8-111">**PnPXCompatibleId**</span></span>](pnpxcompatibleid.md)<br/> | <span data-ttu-id="132a8-112">Especifica el identificador compatible con PnP-X del servicio.</span><span class="sxs-lookup"><span data-stu-id="132a8-112">Specifies the PnP-X Compatible Identifier of the service.</span></span><br/> <br/> |
| [<span data-ttu-id="132a8-113">**PnPXHardwareId**</span><span class="sxs-lookup"><span data-stu-id="132a8-113">**PnPXHardwareId**</span></span>](pnpxhardwareid.md)<br/>     | <span data-ttu-id="132a8-114">Especifica el identificador de hardware PnP-X del servicio.</span><span class="sxs-lookup"><span data-stu-id="132a8-114">Specifies the PnP-X Hardware Identifier of the service.</span></span><br/> <br/>   |
| [<span data-ttu-id="132a8-115">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="132a8-115">**ServiceID**</span></span>](serviceid.md)<br/>               | <span data-ttu-id="132a8-116">Define un identificador de servicio para el host de servicio.</span><span class="sxs-lookup"><span data-stu-id="132a8-116">Defines a service identifier for the service host.</span></span><br/> <br/>        |
| [<span data-ttu-id="132a8-117">**Tipos**</span><span class="sxs-lookup"><span data-stu-id="132a8-117">**Types**</span></span>](types.md)<br/>                       | <span data-ttu-id="132a8-118">Define una lista de nombres completos de XSD.</span><span class="sxs-lookup"><span data-stu-id="132a8-118">Defines a list of XSD qualified names.</span></span><br/> <br/>                    |



### <a name="child-element-sequence"></a><span data-ttu-id="132a8-119">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="132a8-119">Child element sequence</span></span>

``` syntax
(
  ServiceID, 
  Types, 
  PnPXHardwareId?, 
  PnPXCompatibleId?
)
```

## <a name="parent-elements"></a><span data-ttu-id="132a8-120">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="132a8-120">Parent elements</span></span>



| <span data-ttu-id="132a8-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="132a8-121">Element</span></span>                                         | <span data-ttu-id="132a8-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="132a8-122">Description</span></span>                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="132a8-123">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="132a8-123">**hostMetadata**</span></span>](hostmetadata.md)<br/> | <span data-ttu-id="132a8-124">Los metadatos de hospedaje para el dispositivo que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="132a8-124">The hosting metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="132a8-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="132a8-125">Remarks</span></span>

<span data-ttu-id="132a8-126">Cada servicio proporcionado por un host de servicio debe tener su propia información de elemento **hospedado** para asegurarse de que el servicio se publique correctamente en las respuestas a las solicitudes de metadatos.</span><span class="sxs-lookup"><span data-stu-id="132a8-126">Each service provided by a service host should have its own **hosted** element information to ensure that the service is published properly in responses to metadata requests.</span></span>

<span data-ttu-id="132a8-127">Los elementos [**PnPXHardwareId**](pnpxhardwareid.md) y [**PnPXCompatibleId**](pnpxcompatibleid.md) son opcionales, pero cuando se usan, deben usarse juntos.</span><span class="sxs-lookup"><span data-stu-id="132a8-127">The [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements are optional, but when used, they must be used together.</span></span> <span data-ttu-id="132a8-128">Si existe uno, el otro también debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="132a8-128">If one is present, the other must be present as well.</span></span>

<span data-ttu-id="132a8-129">Si hay un elemento [**PnPXDeviceCategory**](pnpxdevicecategory.md) , al menos un elemento **hospedado** debe contener los elementos [**PnPXHardwareId**](pnpxhardwareid.md) y [**PnPXCompatibleId**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="132a8-129">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one **hosted** element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="132a8-130">Del mismo modo, si los elementos **PnPXHardwareId** y **PnPXCompatibleId** están presentes en un elemento **hospedado** , al menos un elemento **PnPXDeviceCategory** debe estar presente dentro del elemento [**thisModelMetadata**](thismodelmetadata.md) .</span><span class="sxs-lookup"><span data-stu-id="132a8-130">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element must be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="132a8-131">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="132a8-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="132a8-132">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="132a8-132">Minimum supported system</span></span><br/> | <span data-ttu-id="132a8-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="132a8-133">Windows Vista</span></span> |
| <span data-ttu-id="132a8-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="132a8-134">Can be empty</span></span>                        | <span data-ttu-id="132a8-135">No</span><span class="sxs-lookup"><span data-stu-id="132a8-135">No</span></span>            |



 

 




