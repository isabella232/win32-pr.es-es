---
description: URI que representa el identificador de servicio.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: Elemento ServiceID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c8b02fa8ecfa936aa658a1f18242e4f14eb0dd
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995112"
---
# <a name="serviceid-element"></a><span data-ttu-id="1f8de-103">Elemento ServiceID</span><span class="sxs-lookup"><span data-stu-id="1f8de-103">ServiceID element</span></span>

<span data-ttu-id="1f8de-104">URI que representa el identificador de servicio.</span><span class="sxs-lookup"><span data-stu-id="1f8de-104">A URI that represents the service identifier.</span></span>

## <a name="usage"></a><span data-ttu-id="1f8de-105">Uso</span><span class="sxs-lookup"><span data-stu-id="1f8de-105">Usage</span></span>

``` syntax
<ServiceID/>
```

## <a name="attributes"></a><span data-ttu-id="1f8de-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="1f8de-106">Attributes</span></span>

<span data-ttu-id="1f8de-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="1f8de-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1f8de-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1f8de-108">Child elements</span></span>

<span data-ttu-id="1f8de-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="1f8de-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="1f8de-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="1f8de-110">Parent elements</span></span>



| <span data-ttu-id="1f8de-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="1f8de-111">Element</span></span>                             | <span data-ttu-id="1f8de-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f8de-112">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f8de-113">**Host**</span><span class="sxs-lookup"><span data-stu-id="1f8de-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="1f8de-114">Define los **elementos ServiceID** y [**Types**](types.md) para el host de servicio.</span><span class="sxs-lookup"><span data-stu-id="1f8de-114">Defines the **ServiceID** and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="1f8de-115">Si no se proporciona explícitamente, WSDAPI no suministrará ningún dato predeterminado en respuesta a las solicitudes de metadatos.</span><span class="sxs-lookup"><span data-stu-id="1f8de-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                     |
| [<span data-ttu-id="1f8de-116">**Alojados**</span><span class="sxs-lookup"><span data-stu-id="1f8de-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="1f8de-117">Define los **elementos ServiceID** y [**Types**](types.md) para los servicios proporcionados por este host de servicio.</span><span class="sxs-lookup"><span data-stu-id="1f8de-117">Defines the **ServiceID** and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="1f8de-118">Cada servicio proporcionado por este host [](hosted.md) de servicio debe tener su propia información de elemento hospedado para asegurarse de que el servicio se publica correctamente en respuestas a solicitudes de metadatos.</span><span class="sxs-lookup"><span data-stu-id="1f8de-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="1f8de-119">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1f8de-119">Element information</span></span>



| <span data-ttu-id="1f8de-120">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="1f8de-120">Label</span></span> | <span data-ttu-id="1f8de-121">Value</span><span class="sxs-lookup"><span data-stu-id="1f8de-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="1f8de-122">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f8de-122">Minimum supported system</span></span><br/> | <span data-ttu-id="1f8de-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f8de-123">Windows Vista</span></span> |
| <span data-ttu-id="1f8de-124">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1f8de-124">Can be empty</span></span>                        | <span data-ttu-id="1f8de-125">Sí</span><span class="sxs-lookup"><span data-stu-id="1f8de-125">Yes</span></span>           |



 

 




