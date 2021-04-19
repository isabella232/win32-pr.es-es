---
description: URI que representa el identificador del servicio.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: Elemento ServiceID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305e97250b0b33d276dced4b5d454aec9298387c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707256"
---
# <a name="serviceid-element"></a><span data-ttu-id="e10f5-103">Elemento ServiceID</span><span class="sxs-lookup"><span data-stu-id="e10f5-103">ServiceID element</span></span>

<span data-ttu-id="e10f5-104">URI que representa el identificador del servicio.</span><span class="sxs-lookup"><span data-stu-id="e10f5-104">A URI that represents the service identifier.</span></span>

## <a name="usage"></a><span data-ttu-id="e10f5-105">Uso</span><span class="sxs-lookup"><span data-stu-id="e10f5-105">Usage</span></span>

``` syntax
<ServiceID/>
```

## <a name="attributes"></a><span data-ttu-id="e10f5-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="e10f5-106">Attributes</span></span>

<span data-ttu-id="e10f5-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="e10f5-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e10f5-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e10f5-108">Child elements</span></span>

<span data-ttu-id="e10f5-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="e10f5-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="e10f5-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="e10f5-110">Parent elements</span></span>



| <span data-ttu-id="e10f5-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="e10f5-111">Element</span></span>                             | <span data-ttu-id="e10f5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e10f5-112">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e10f5-113">**organizar**</span><span class="sxs-lookup"><span data-stu-id="e10f5-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="e10f5-114">Define los elementos **ServiceID** y [**Types**](types.md) para el host de servicio.</span><span class="sxs-lookup"><span data-stu-id="e10f5-114">Defines the **ServiceID** and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="e10f5-115">Si no se proporciona explícitamente, WSDAPI no proporcionará datos predeterminados en respuesta a las solicitudes de metadatos.</span><span class="sxs-lookup"><span data-stu-id="e10f5-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                     |
| [<span data-ttu-id="e10f5-116">**ubicada**</span><span class="sxs-lookup"><span data-stu-id="e10f5-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="e10f5-117">Define los elementos **ServiceID** y [**Types**](types.md) para los servicios proporcionados por este host de servicio.</span><span class="sxs-lookup"><span data-stu-id="e10f5-117">Defines the **ServiceID** and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="e10f5-118">Cada servicio proporcionado por este host de servicio debe tener su propia información de elemento [**hospedado**](hosted.md) para asegurarse de que el servicio se publique correctamente en las respuestas a las solicitudes de metadatos.</span><span class="sxs-lookup"><span data-stu-id="e10f5-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="e10f5-119">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e10f5-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="e10f5-120">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e10f5-120">Minimum supported system</span></span><br/> | <span data-ttu-id="e10f5-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e10f5-121">Windows Vista</span></span> |
| <span data-ttu-id="e10f5-122">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e10f5-122">Can be empty</span></span>                        | <span data-ttu-id="e10f5-123">Sí</span><span class="sxs-lookup"><span data-stu-id="e10f5-123">Yes</span></span>           |



 

 




