---
title: Tiendas en línea privadas
description: Tiendas en línea privadas
ms.assetid: c1e241f5-6d29-4b53-8be0-264597e03de7
keywords:
- Windows Media Player tiendas en línea, privado
- tiendas en línea, privado
- tipo 1 tiendas en línea, privado
- tipo 2 tiendas en línea, privado
- tiendas en línea privadas
- registro, almacenes privados en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e11490a8a12659dfc1e2c5445167e8d71abaf00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418889"
---
# <a name="private-online-stores"></a><span data-ttu-id="40054-109">Tiendas en línea privadas</span><span class="sxs-lookup"><span data-stu-id="40054-109">Private Online Stores</span></span>

<span data-ttu-id="40054-110">Windows Media Player 10 o posterior admite tiendas en línea privadas; es decir, los almacenes que solo son visibles para determinados usuarios.</span><span class="sxs-lookup"><span data-stu-id="40054-110">Windows Media Player 10 or later supports private online stores; that is, stores that are visible only to certain users.</span></span> <span data-ttu-id="40054-111">Para que una tienda en línea privada sea visible para el usuario actual, debe haber una entrada que represente la tienda en línea privada en la siguiente clave del registro.</span><span class="sxs-lookup"><span data-stu-id="40054-111">For a private online store to be visible to the current user, there must be an entry that represents the private online store under the following registry key.</span></span>

<span data-ttu-id="40054-112">HKEY \_ Current \_ User \\ software \\ Microsoft \\ MediaPlayer \\ PrivateServices</span><span class="sxs-lookup"><span data-stu-id="40054-112">HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\PrivateServices</span></span>

<span data-ttu-id="40054-113">La entrada del registro requerida debe tener el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="40054-113">The required registry entry must have the following format.</span></span>



| <span data-ttu-id="40054-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="40054-114">Name</span></span>                                                         | <span data-ttu-id="40054-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="40054-115">Type</span></span>           | <span data-ttu-id="40054-116">Value</span><span class="sxs-lookup"><span data-stu-id="40054-116">Value</span></span>                                                                     |
|--------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="40054-117">Cualquier nombre elegido por la persona que crea la entrada del registro</span><span class="sxs-lookup"><span data-stu-id="40054-117">Any name chosen by the person who creates the registry entry</span></span> | <span data-ttu-id="40054-118">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="40054-118">**REG\_DWORD**</span></span> | <span data-ttu-id="40054-119">Un número, proporcionado por Microsoft, que identifica la tienda en línea privada.</span><span class="sxs-lookup"><span data-stu-id="40054-119">A number, provided by Microsoft, that identifies the private online store</span></span> |



 

<span data-ttu-id="40054-120">El control ActiveX de Windows Media Player 10 solo admite tiendas en línea privadas si el control se está ejecutando en modo remoto.</span><span class="sxs-lookup"><span data-stu-id="40054-120">The Windows Media Player 10 ActiveX control supports private online stores only if the control is running in remote mode.</span></span> <span data-ttu-id="40054-121">El control ActiveX de Windows Media Player 11 admite almacenes en línea privados, independientemente de si el control se está ejecutando en modo remoto.</span><span class="sxs-lookup"><span data-stu-id="40054-121">The Windows Media Player 11 ActiveX control supports private online stores regardless of whether the control is running in remote mode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40054-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40054-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40054-123">**Información común para las tiendas en línea de tipo 1 y 2**</span><span class="sxs-lookup"><span data-stu-id="40054-123">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




