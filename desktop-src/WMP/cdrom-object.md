---
title: CDROM (objeto)
description: El objeto CDROM proporciona una manera de tener acceso a un CD o DVD en su unidad.
ms.assetid: 9045b130-3e08-4880-a4e7-79b704c4c1f9
keywords:
- Objeto CDROM Media Player de Windows
topic_type:
- apiref
api_name:
- Cdrom Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17c2de88749b4dd4a0ab756b77866c16e8878486
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104357901"
---
# <a name="cdrom-object"></a><span data-ttu-id="dfb5c-104">CDROM (objeto)</span><span class="sxs-lookup"><span data-stu-id="dfb5c-104">Cdrom Object</span></span>

<span data-ttu-id="dfb5c-105">El objeto **CDROM** proporciona una manera de tener acceso a un CD o DVD en su unidad.</span><span class="sxs-lookup"><span data-stu-id="dfb5c-105">The **Cdrom** object provides a way to access a CD or DVD in its drive.</span></span>

<span data-ttu-id="dfb5c-106">El objeto **CDROM** admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="dfb5c-106">The **Cdrom** object supports the following properties.</span></span>



| <span data-ttu-id="dfb5c-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dfb5c-107">Property</span></span>                                   | <span data-ttu-id="dfb5c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfb5c-108">Description</span></span>                                                                                                                                             |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dfb5c-109">driveSpecifier</span><span class="sxs-lookup"><span data-stu-id="dfb5c-109">driveSpecifier</span></span>](cdrom-drivespecifier.md) | <span data-ttu-id="dfb5c-110">Recupera la letra de unidad de CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="dfb5c-110">Retrieves the CD or DVD drive letter.</span></span>                                                                                                                   |
| [<span data-ttu-id="dfb5c-111">automáticas</span><span class="sxs-lookup"><span data-stu-id="dfb5c-111">playlist</span></span>](cdrom-playlist.md)             | <span data-ttu-id="dfb5c-112">Recupera un objeto de [lista de reproducción](playlist-object.md) que representa las pistas del CD que se encuentran actualmente en la unidad de CD o en las entradas de título de nivel de raíz de DVD.</span><span class="sxs-lookup"><span data-stu-id="dfb5c-112">Retrieves a [Playlist](playlist-object.md) object representing the tracks on the CD currently in the CD drive or the root-level title entries for DVD.</span></span> |



 

<span data-ttu-id="dfb5c-113">El objeto **CDROM** admite el método siguiente.</span><span class="sxs-lookup"><span data-stu-id="dfb5c-113">The **Cdrom** object supports the following method.</span></span>



| <span data-ttu-id="dfb5c-114">Método</span><span class="sxs-lookup"><span data-stu-id="dfb5c-114">Method</span></span>                   | <span data-ttu-id="dfb5c-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfb5c-115">Description</span></span>                          |
|--------------------------|--------------------------------------|
| [<span data-ttu-id="dfb5c-116">expulsar</span><span class="sxs-lookup"><span data-stu-id="dfb5c-116">eject</span></span>](cdrom-eject.md) | <span data-ttu-id="dfb5c-117">Expulsa el CD o DVD de la unidad.</span><span class="sxs-lookup"><span data-stu-id="dfb5c-117">Ejects the CD or DVD from the drive.</span></span> |



 

<span data-ttu-id="dfb5c-118">Se tiene acceso al objeto **CDROM** mediante el método siguiente.</span><span class="sxs-lookup"><span data-stu-id="dfb5c-118">The **Cdrom** object is accessed through the following method.</span></span>



| <span data-ttu-id="dfb5c-119">Object</span><span class="sxs-lookup"><span data-stu-id="dfb5c-119">Object</span></span>                                        | <span data-ttu-id="dfb5c-120">Método</span><span class="sxs-lookup"><span data-stu-id="dfb5c-120">Method</span></span>                           |
|-----------------------------------------------|----------------------------------|
| [<span data-ttu-id="dfb5c-121">CdromCollection</span><span class="sxs-lookup"><span data-stu-id="dfb5c-121">CdromCollection</span></span>](cdromcollection-object.md) | [<span data-ttu-id="dfb5c-122">item</span><span class="sxs-lookup"><span data-stu-id="dfb5c-122">item</span></span>](cdromcollection-item.md) |



 

<span data-ttu-id="dfb5c-123">A efectos de Ilustración, se usa Player. cdromCollection. Item (*index*) en las secciones de sintaxis de referencia.</span><span class="sxs-lookup"><span data-stu-id="dfb5c-123">For purposes of illustration, player.cdromCollection.item(*index*) is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="dfb5c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfb5c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfb5c-125">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="dfb5c-125">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




