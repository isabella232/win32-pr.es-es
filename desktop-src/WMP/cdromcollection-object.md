---
title: Objeto CdromCollection
description: El objeto CdromCollection proporciona una manera de organizar y obtener acceso a una colección de unidades de CD o DVD.
ms.assetid: 02429ba7-a053-42bf-9ed5-c05e13c964c0
keywords:
- Objeto CdromCollection Media Player de Windows
topic_type:
- apiref
api_name:
- CdromCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d5367a6887290f06d36225f211f42048e98ba03
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076492"
---
# <a name="cdromcollection-object"></a><span data-ttu-id="33593-104">Objeto CdromCollection</span><span class="sxs-lookup"><span data-stu-id="33593-104">CdromCollection Object</span></span>

<span data-ttu-id="33593-105">El objeto **CdromCollection** proporciona una manera de organizar y obtener acceso a una colección de unidades de CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="33593-105">The **CdromCollection** object provides a way to organize and access a collection of CD or DVD drives.</span></span>

<span data-ttu-id="33593-106">El objeto **CdromCollection** admite la siguiente propiedad.</span><span class="sxs-lookup"><span data-stu-id="33593-106">The **CdromCollection** object supports the following property.</span></span>



| <span data-ttu-id="33593-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="33593-107">Property</span></span>                           | <span data-ttu-id="33593-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="33593-108">Description</span></span>                                                        |
|------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="33593-109">count</span><span class="sxs-lookup"><span data-stu-id="33593-109">count</span></span>](cdromcollection-count.md) | <span data-ttu-id="33593-110">Recupera el número de unidades de CD y DVD disponibles en el sistema.</span><span class="sxs-lookup"><span data-stu-id="33593-110">Retrieves the number of available CD and DVD drives on the system.</span></span> |



 

<span data-ttu-id="33593-111">El objeto **CdromCollection** admite los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="33593-111">The **CdromCollection** object supports the following methods.</span></span>



| <span data-ttu-id="33593-112">Método</span><span class="sxs-lookup"><span data-stu-id="33593-112">Method</span></span>                                                         | <span data-ttu-id="33593-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="33593-113">Description</span></span>                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33593-114">getByDriveSpecifier</span><span class="sxs-lookup"><span data-stu-id="33593-114">getByDriveSpecifier</span></span>](cdromcollection-getbydrivespecifier.md) | <span data-ttu-id="33593-115">Recupera el objeto [CDROM](cdrom-object.md) asociado a una letra de unidad concreta.</span><span class="sxs-lookup"><span data-stu-id="33593-115">Retrieves the [Cdrom](cdrom-object.md) object associated with a particular drive letter.</span></span> |
| [<span data-ttu-id="33593-116">item</span><span class="sxs-lookup"><span data-stu-id="33593-116">item</span></span>](cdromcollection-item.md)                               | <span data-ttu-id="33593-117">Recupera el objeto [CDROM](cdrom-object.md) en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="33593-117">Retrieves the [Cdrom](cdrom-object.md) object at the given index.</span></span>                        |



 

<span data-ttu-id="33593-118">Se tiene acceso al objeto **CdromCollection** a través de la propiedad siguiente.</span><span class="sxs-lookup"><span data-stu-id="33593-118">The **CdromCollection** object is accessed through the following property.</span></span>



| <span data-ttu-id="33593-119">Object</span><span class="sxs-lookup"><span data-stu-id="33593-119">Object</span></span>                      | <span data-ttu-id="33593-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="33593-120">Property</span></span>                                      |
|-----------------------------|-----------------------------------------------|
| [<span data-ttu-id="33593-121">Reproductor</span><span class="sxs-lookup"><span data-stu-id="33593-121">Player</span></span>](player-object.md) | [<span data-ttu-id="33593-122">cdromCollection</span><span class="sxs-lookup"><span data-stu-id="33593-122">cdromCollection</span></span>](player-cdromcollection.md) |



 

## <a name="see-also"></a><span data-ttu-id="33593-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="33593-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33593-124">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="33593-124">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




