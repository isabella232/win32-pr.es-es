---
description: Define los elementos ServiceID, Types,PnPXHardwareId y PnPXCompatibleId para los servicios definidos por el host de servicio.
ms.assetid: f901a88f-7e01-4e7f-a0f2-59f2a01b03cd
title: elemento hospedado
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3d281b5e058f8716c12c655ebcdb9a17bdfa4fb
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994892"
---
# <a name="hosted-element"></a><span data-ttu-id="7ab2e-103">elemento hospedado</span><span class="sxs-lookup"><span data-stu-id="7ab2e-103">hosted element</span></span>

<span data-ttu-id="7ab2e-104">Define los [**elementos ServiceID**](serviceid.md), [**Types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md)y [**PnPXCompatibleId**](pnpxcompatibleid.md) para los servicios definidos por el host de servicio.</span><span class="sxs-lookup"><span data-stu-id="7ab2e-104">Defines the [**ServiceID**](serviceid.md), [**Types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md), and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements for the services defined by the service host.</span></span>

## <a name="usage"></a><span data-ttu-id="7ab2e-105">Uso</span><span class="sxs-lookup"><span data-stu-id="7ab2e-105">Usage</span></span>

``` syntax
<hosted>
  child elements
</hosted>
```

## <a name="attributes"></a><span data-ttu-id="7ab2e-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="7ab2e-106">Attributes</span></span>

<span data-ttu-id="7ab2e-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="7ab2e-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7ab2e-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7ab2e-108">Child elements</span></span>



| <span data-ttu-id="7ab2e-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="7ab2e-109">Element</span></span>                                                 | <span data-ttu-id="7ab2e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ab2e-110">Description</span></span>                                                                      |
|---------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="7ab2e-111">**PnPXCompatibleId**</span><span class="sxs-lookup"><span data-stu-id="7ab2e-111">**PnPXCompatibleId**</span></span>](pnpxcompatibleid.md)<br/> | <span data-ttu-id="7ab2e-112">Especifica el identificador compatible con PnP-X del servicio.</span><span class="sxs-lookup"><span data-stu-id="7ab2e-112">Specifies the PnP-X Compatible Identifier of the service.</span></span><br/> <br/> |
| [<span data-ttu-id="7ab2e-113">**PnPXHardwareId**</span><span class="sxs-lookup"><span data-stu-id="7ab2e-113">**PnPXHardwareId**</span></span>](pnpxhardwareid.md)<br/>     | <span data-ttu-id="7ab2e-114">Especifica el identificador de hardware PnP-X del servicio.</span><span class="sxs-lookup"><span data-stu-id="7ab2e-114">Specifies the PnP-X Hardware Identifier of the service.</span></span><br/> <br/>   |
| [<span data-ttu-id="7ab2e-115">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="7ab2e-115">**ServiceID**</span></span>](serviceid.md)<br/>               | <span data-ttu-id="7ab2e-116">Define un identificador de servicio para el host de servicio.</span><span class="sxs-lookup"><span data-stu-id="7ab2e-116">Defines a service identifier for the service host.</span></span><br/> <br/>        |
| [<span data-ttu-id="7ab2e-117">**Tipos**</span><span class="sxs-lookup"><span data-stu-id="7ab2e-117">**Types**</span></span>](types.md)<br/>                       | <span data-ttu-id="7ab2e-118">Define una lista de nombres completos XSD.</span><span class="sxs-lookup"><span data-stu-id="7ab2e-118">Defines a list of XSD qualified names.</span></span><br/> <br/>                    |



### <a name="child-element-sequence"></a><span data-ttu-id="7ab2e-119">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7ab2e-119">Child element sequence</span></span>

``` syntax
(
  ServiceID, 
  Types, 
  PnPXHardwareId?, 
  PnPXCompatibleId?
)
```

## <a name="parent-elements"></a><span data-ttu-id="7ab2e-120">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="7ab2e-120">Parent elements</span></span>



| <span data-ttu-id="7ab2e-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="7ab2e-121">Element</span></span>                                         | <span data-ttu-id="7ab2e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ab2e-122">Description</span></span>                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="7ab2e-123">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="7ab2e-123">**hostMetadata**</span></span>](hostmetadata.md)<br/> | <span data-ttu-id="7ab2e-124">Metadatos de hospedaje para el dispositivo que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="7ab2e-124">The hosting metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="7ab2e-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7ab2e-125">Remarks</span></span>

<span data-ttu-id="7ab2e-126">Cada servicio proporcionado por un host  de servicio debe tener su propia información de elemento hospedado para asegurarse de que el servicio se publica correctamente en respuestas a solicitudes de metadatos.</span><span class="sxs-lookup"><span data-stu-id="7ab2e-126">Each service provided by a service host should have its own **hosted** element information to ensure that the service is published properly in responses to metadata requests.</span></span>

<span data-ttu-id="7ab2e-127">Los [**elementos PnPXHardwareId**](pnpxhardwareid.md) y [**PnPXCompatibleId**](pnpxcompatibleid.md) son opcionales, pero cuando se usan, deben usarse juntos.</span><span class="sxs-lookup"><span data-stu-id="7ab2e-127">The [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements are optional, but when used, they must be used together.</span></span> <span data-ttu-id="7ab2e-128">Si uno está presente, el otro también debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="7ab2e-128">If one is present, the other must be present as well.</span></span>

<span data-ttu-id="7ab2e-129">Si hay [**un elemento PnPXDeviceCategory,**](pnpxdevicecategory.md)  al menos un elemento hospedado debe contener los elementos [**PnPXHardwareId**](pnpxhardwareid.md) y [**PnPXCompatibleId.**](pnpxcompatibleid.md)</span><span class="sxs-lookup"><span data-stu-id="7ab2e-129">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one **hosted** element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="7ab2e-130">Del mismo modo, si los elementos **PnPXHardwareId** y  **PnPXCompatibleId** están presentes en un elemento hospedado, debe haber al menos un elemento **PnPXDeviceCategory** dentro del [**elemento thisModelMetadata.**](thismodelmetadata.md)</span><span class="sxs-lookup"><span data-stu-id="7ab2e-130">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element must be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="7ab2e-131">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7ab2e-131">Element information</span></span>



| <span data-ttu-id="7ab2e-132">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="7ab2e-132">Label</span></span> | <span data-ttu-id="7ab2e-133">Value</span><span class="sxs-lookup"><span data-stu-id="7ab2e-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="7ab2e-134">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ab2e-134">Minimum supported system</span></span><br/> | <span data-ttu-id="7ab2e-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ab2e-135">Windows Vista</span></span> |
| <span data-ttu-id="7ab2e-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7ab2e-136">Can be empty</span></span>                        | <span data-ttu-id="7ab2e-137">No</span><span class="sxs-lookup"><span data-stu-id="7ab2e-137">No</span></span>            |



 

 




