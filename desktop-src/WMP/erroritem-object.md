---
title: Objeto ErrorItem
description: El objeto ErrorItem proporciona una manera de tener acceso a la información de errores.
ms.assetid: 14bc9c12-98c6-4b72-9ae5-d6afeb1303f9
keywords:
- Objeto ErrorItem Media Player de Windows
topic_type:
- apiref
api_name:
- ErrorItem Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c273d00477363c66c49dfa1f77a66dab42c711cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105695504"
---
# <a name="erroritem-object"></a><span data-ttu-id="d58a8-104">Objeto ErrorItem</span><span class="sxs-lookup"><span data-stu-id="d58a8-104">ErrorItem Object</span></span>

<span data-ttu-id="d58a8-105">El objeto **ErrorItem** proporciona una manera de tener acceso a la información de errores.</span><span class="sxs-lookup"><span data-stu-id="d58a8-105">The **ErrorItem** object provides a way to access error information.</span></span>

<span data-ttu-id="d58a8-106">El objeto **ErrorItem** admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="d58a8-106">The **ErrorItem** object supports the following properties.</span></span>



| <span data-ttu-id="d58a8-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d58a8-107">Property</span></span>                                           | <span data-ttu-id="d58a8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d58a8-108">Description</span></span>                                                                                     |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d58a8-109">condition</span><span class="sxs-lookup"><span data-stu-id="d58a8-109">condition</span></span>](erroritem-condition.md)               | <span data-ttu-id="d58a8-110">Recupera un valor que indica la condición del error.</span><span class="sxs-lookup"><span data-stu-id="d58a8-110">Retrieves a value indicating the condition for the error.</span></span>                                       |
| [<span data-ttu-id="d58a8-111">customUrl</span><span class="sxs-lookup"><span data-stu-id="d58a8-111">customUrl</span></span>](erroritem-customurl.md)               | <span data-ttu-id="d58a8-112">Recupera la dirección URL de un sitio web que muestra información específica sobre el error de descarga de códec.</span><span class="sxs-lookup"><span data-stu-id="d58a8-112">Retrieves the URL of a website that displays specific information about codec download failure.</span></span> |
| [<span data-ttu-id="d58a8-113">errorCode</span><span class="sxs-lookup"><span data-stu-id="d58a8-113">errorCode</span></span>](erroritem-errorcode.md)               | <span data-ttu-id="d58a8-114">Recupera el código de error actual.</span><span class="sxs-lookup"><span data-stu-id="d58a8-114">Retrieves the current error code.</span></span>                                                               |
| [<span data-ttu-id="d58a8-115">errorContext</span><span class="sxs-lookup"><span data-stu-id="d58a8-115">errorContext</span></span>](erroritem-errorcontext.md)         | <span data-ttu-id="d58a8-116">Recupera un valor que indica el contexto del error.</span><span class="sxs-lookup"><span data-stu-id="d58a8-116">Retrieves a value indicating the context of the error.</span></span>                                          |
| [<span data-ttu-id="d58a8-117">errorDescription</span><span class="sxs-lookup"><span data-stu-id="d58a8-117">errorDescription</span></span>](erroritem-errordescription.md) | <span data-ttu-id="d58a8-118">Recupera una descripción del error.</span><span class="sxs-lookup"><span data-stu-id="d58a8-118">Retrieves a description of the error.</span></span>                                                           |
| <span data-ttu-id="d58a8-119">**remedio**</span><span class="sxs-lookup"><span data-stu-id="d58a8-119">**remedy**</span></span>                                         | <span data-ttu-id="d58a8-120">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d58a8-120">Reserved for future use.</span></span>                                                                        |



 

<span data-ttu-id="d58a8-121">Se tiene acceso al objeto **ErrorItem** a través de los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="d58a8-121">The **ErrorItem** object is accessed through the following methods.</span></span>



| <span data-ttu-id="d58a8-122">Object</span><span class="sxs-lookup"><span data-stu-id="d58a8-122">Object</span></span>                    | <span data-ttu-id="d58a8-123">Método</span><span class="sxs-lookup"><span data-stu-id="d58a8-123">Method</span></span>                   |
|---------------------------|--------------------------|
| [<span data-ttu-id="d58a8-124">Error</span><span class="sxs-lookup"><span data-stu-id="d58a8-124">Error</span></span>](error-object.md) | [<span data-ttu-id="d58a8-125">item</span><span class="sxs-lookup"><span data-stu-id="d58a8-125">item</span></span>](error-item.md)   |
| [<span data-ttu-id="d58a8-126">Elementos multimedia</span><span class="sxs-lookup"><span data-stu-id="d58a8-126">Media</span></span>](media-object.md) | [<span data-ttu-id="d58a8-127">error</span><span class="sxs-lookup"><span data-stu-id="d58a8-127">error</span></span>](media-error.md) |



 

<span data-ttu-id="d58a8-128">Para fines de Ilustración, *reproductor*. *error*. *Item*(*index*) se usa en las secciones de sintaxis de referencia.</span><span class="sxs-lookup"><span data-stu-id="d58a8-128">For purposes of illustration, *player*.*error*.*item*(*index*) is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="d58a8-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d58a8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d58a8-130">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="d58a8-130">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




