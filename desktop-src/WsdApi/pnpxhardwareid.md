---
description: Especifica el identificador de hardware PnP-X del servicio.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Elemento PnPXHardwareId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55e5e38b669a289545225df96fad05e55069b474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696903"
---
# <a name="pnpxhardwareid-element"></a><span data-ttu-id="81c93-103">Elemento PnPXHardwareId</span><span class="sxs-lookup"><span data-stu-id="81c93-103">PnPXHardwareId element</span></span>

<span data-ttu-id="81c93-104">Especifica el identificador de hardware PnP-X del servicio.</span><span class="sxs-lookup"><span data-stu-id="81c93-104">Specifies the PnP-X Hardware Identifier of the service.</span></span> <span data-ttu-id="81c93-105">PnP coincide con este elemento con las descripciones de hardware proporcionadas en la \[ \] sección PnpxDevice del archivo INF del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81c93-105">PnP matches this element with the hardware description(s) provided in the \[PnpxDevice\] section of the device's INF file.</span></span> <span data-ttu-id="81c93-106">En función de esta información, el servicio PnP selecciona y carga el controlador de dispositivo más adecuado.</span><span class="sxs-lookup"><span data-stu-id="81c93-106">Based on this information, the PnP service selects and loads the most appropriate device driver.</span></span>

## <a name="usage"></a><span data-ttu-id="81c93-107">Uso</span><span class="sxs-lookup"><span data-stu-id="81c93-107">Usage</span></span>

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a><span data-ttu-id="81c93-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="81c93-108">Attributes</span></span>

<span data-ttu-id="81c93-109">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="81c93-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="81c93-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="81c93-110">Child elements</span></span>

<span data-ttu-id="81c93-111">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="81c93-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="81c93-112">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="81c93-112">Parent elements</span></span>



| <span data-ttu-id="81c93-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="81c93-113">Element</span></span>                             | <span data-ttu-id="81c93-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="81c93-114">Description</span></span>                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="81c93-115">**ubicada**</span><span class="sxs-lookup"><span data-stu-id="81c93-115">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="81c93-116">Define los elementos para los servicios definidos por el host de servicio.</span><span class="sxs-lookup"><span data-stu-id="81c93-116">Defines elements for the services defined by the service host.</span></span> <br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="81c93-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81c93-117">Remarks</span></span>

<span data-ttu-id="81c93-118">Para especificar más de un identificador de hardware, separe los identificadores con un carácter de espacio, por ejemplo, "PnPX SampleService de juegos de software \_ \_ \_ 1 PnPX SampleService de hardware \_ \_ \_ 2 PnPX \_ SampleService1 de \_ hardware \_ 3".</span><span class="sxs-lookup"><span data-stu-id="81c93-118">To specify more than one hardware ID, separate the identifiers with a space character, for example, "PnPX\_SampleService\_HWID\_1 PnPX\_SampleService\_HWID\_2 PnPX\_SampleService1\_HWID\_3".</span></span>

## <a name="element-information"></a><span data-ttu-id="81c93-119">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="81c93-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="81c93-120">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81c93-120">Minimum supported system</span></span><br/> | <span data-ttu-id="81c93-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81c93-121">Windows Vista</span></span> |
| <span data-ttu-id="81c93-122">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="81c93-122">Can be empty</span></span>                        | <span data-ttu-id="81c93-123">Sí</span><span class="sxs-lookup"><span data-stu-id="81c93-123">Yes</span></span>           |



 

 




