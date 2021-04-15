---
title: Error (objeto, WMP SDK)
description: El objeto error proporciona acceso a una colección de objetos ErrorItem.
ms.assetid: 1f026ad4-0240-48fe-90ad-739a24e8a7ca
keywords:
- Objeto de error de Windows Media Player
topic_type:
- apiref
api_name:
- Error Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0aae4c86dc3f5282be7a16207923e1238e217a9e
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/09/2019
ms.locfileid: "105695520"
---
# <a name="error-object"></a><span data-ttu-id="cc50d-104">Objeto de error</span><span class="sxs-lookup"><span data-stu-id="cc50d-104">Error Object</span></span>

<span data-ttu-id="cc50d-105">El objeto **error** proporciona acceso a una colección de objetos [ErrorItem](erroritem-object.md) .</span><span class="sxs-lookup"><span data-stu-id="cc50d-105">The **Error** object provides access to a collection of [ErrorItem](erroritem-object.md) objects.</span></span>

<span data-ttu-id="cc50d-106">El objeto **error** admite la siguiente propiedad.</span><span class="sxs-lookup"><span data-stu-id="cc50d-106">The **Error** object supports the following property.</span></span>



| <span data-ttu-id="cc50d-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cc50d-107">Property</span></span>                           | <span data-ttu-id="cc50d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc50d-108">Description</span></span>                                        |
|------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="cc50d-109">errorCount</span><span class="sxs-lookup"><span data-stu-id="cc50d-109">errorCount</span></span>](error-errorcount.md) | <span data-ttu-id="cc50d-110">Recupera el número de errores en la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="cc50d-110">Retrieves the number of errors in the error queue.</span></span> |



 

<span data-ttu-id="cc50d-111">El objeto **error** admite los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="cc50d-111">The **Error** object supports the following methods.</span></span>



| <span data-ttu-id="cc50d-112">Método</span><span class="sxs-lookup"><span data-stu-id="cc50d-112">Method</span></span>                                       | <span data-ttu-id="cc50d-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc50d-113">Description</span></span>                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc50d-114">clearErrorQueue</span><span class="sxs-lookup"><span data-stu-id="cc50d-114">clearErrorQueue</span></span>](error-clearerrorqueue.md) | <span data-ttu-id="cc50d-115">Borra los errores de la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="cc50d-115">Clears the errors from the error queue.</span></span>                                                         |
| [<span data-ttu-id="cc50d-116">item</span><span class="sxs-lookup"><span data-stu-id="cc50d-116">item</span></span>](error-item.md)                       | <span data-ttu-id="cc50d-117">Recupera un objeto [ErrorItem](erroritem-object.md) de la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="cc50d-117">Retrieves an [ErrorItem](erroritem-object.md) object from the error queue.</span></span>                     |
| [<span data-ttu-id="cc50d-118">WebHelp</span><span class="sxs-lookup"><span data-stu-id="cc50d-118">webHelp</span></span>](error-webhelp.md)                 | <span data-ttu-id="cc50d-119">Inicia la página de ayuda Web de Windows Media Player para mostrar información adicional sobre el error.</span><span class="sxs-lookup"><span data-stu-id="cc50d-119">Launches the Windows Media Player Web Help page to display further information about the error.</span></span> |



 

<span data-ttu-id="cc50d-120">Se tiene acceso al objeto de **error** a través de la propiedad siguiente.</span><span class="sxs-lookup"><span data-stu-id="cc50d-120">The **Error** object is accessed through the following property.</span></span>



| <span data-ttu-id="cc50d-121">Object</span><span class="sxs-lookup"><span data-stu-id="cc50d-121">Object</span></span>                      | <span data-ttu-id="cc50d-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cc50d-122">Property</span></span>                  |
|-----------------------------|---------------------------|
| [<span data-ttu-id="cc50d-123">Reproductor</span><span class="sxs-lookup"><span data-stu-id="cc50d-123">Player</span></span>](player-object.md) | [<span data-ttu-id="cc50d-124">error</span><span class="sxs-lookup"><span data-stu-id="cc50d-124">error</span></span>](player-error.md) |



 

## <a name="see-also"></a><span data-ttu-id="cc50d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc50d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc50d-126">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="cc50d-126">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




