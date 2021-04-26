---
description: Especifica el identificador de hardware PnP-X del servicio.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Elemento PnPXHardwareId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0ffc389ca6df363439dd6463b3f86ca756359e8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996532"
---
# <a name="pnpxhardwareid-element"></a><span data-ttu-id="024e2-103">Elemento PnPXHardwareId</span><span class="sxs-lookup"><span data-stu-id="024e2-103">PnPXHardwareId element</span></span>

<span data-ttu-id="024e2-104">Especifica el identificador de hardware PnP-X del servicio.</span><span class="sxs-lookup"><span data-stu-id="024e2-104">Specifies the PnP-X Hardware Identifier of the service.</span></span> <span data-ttu-id="024e2-105">PnP coincide con este elemento con las descripciones de hardware proporcionadas en la \[ sección PnpxDevice \] del archivo INF del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="024e2-105">PnP matches this element with the hardware description(s) provided in the \[PnpxDevice\] section of the device's INF file.</span></span> <span data-ttu-id="024e2-106">En función de esta información, el servicio PnP selecciona y carga el controlador de dispositivo más adecuado.</span><span class="sxs-lookup"><span data-stu-id="024e2-106">Based on this information, the PnP service selects and loads the most appropriate device driver.</span></span>

## <a name="usage"></a><span data-ttu-id="024e2-107">Uso</span><span class="sxs-lookup"><span data-stu-id="024e2-107">Usage</span></span>

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a><span data-ttu-id="024e2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="024e2-108">Attributes</span></span>

<span data-ttu-id="024e2-109">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="024e2-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="024e2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="024e2-110">Child elements</span></span>

<span data-ttu-id="024e2-111">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="024e2-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="024e2-112">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="024e2-112">Parent elements</span></span>



| <span data-ttu-id="024e2-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="024e2-113">Element</span></span>                             | <span data-ttu-id="024e2-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="024e2-114">Description</span></span>                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="024e2-115">**Alojados**</span><span class="sxs-lookup"><span data-stu-id="024e2-115">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="024e2-116">Define elementos para los servicios definidos por el host de servicio.</span><span class="sxs-lookup"><span data-stu-id="024e2-116">Defines elements for the services defined by the service host.</span></span> <br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="024e2-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="024e2-117">Remarks</span></span>

<span data-ttu-id="024e2-118">Para especificar más de un identificador de hardware, separe los identificadores con un carácter de espacio, por ejemplo, "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX \_ SampleService1 \_ HWID \_ 3".</span><span class="sxs-lookup"><span data-stu-id="024e2-118">To specify more than one hardware ID, separate the identifiers with a space character, for example, "PnPX\_SampleService\_HWID\_1 PnPX\_SampleService\_HWID\_2 PnPX\_SampleService1\_HWID\_3".</span></span>

## <a name="element-information"></a><span data-ttu-id="024e2-119">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="024e2-119">Element information</span></span>



| <span data-ttu-id="024e2-120">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="024e2-120">Label</span></span> | <span data-ttu-id="024e2-121">Value</span><span class="sxs-lookup"><span data-stu-id="024e2-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="024e2-122">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="024e2-122">Minimum supported system</span></span><br/> | <span data-ttu-id="024e2-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="024e2-123">Windows Vista</span></span> |
| <span data-ttu-id="024e2-124">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="024e2-124">Can be empty</span></span>                        | <span data-ttu-id="024e2-125">Sí</span><span class="sxs-lookup"><span data-stu-id="024e2-125">Yes</span></span>           |



 

 




