---
title: Almacén de licencias local
description: Almacén de licencias local
ms.assetid: f50e4535-1d4d-4486-8308-c3314b1f5414
keywords:
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- SDK de Windows Media Format, licencias de DRM
- SDK de Windows Media Format, licencias de DRM
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- Administración de derechos digitales (DRM), licencias de archivos protegidos
- DRM (administración de derechos digitales), licencias de archivos protegidos
- licencias, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d28703a0387d8676c4c8d5bf08f9e27a3ecf5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419132"
---
# <a name="local-license-store"></a><span data-ttu-id="54fea-111">Almacén de licencias local</span><span class="sxs-lookup"><span data-stu-id="54fea-111">Local License Store</span></span>

<span data-ttu-id="54fea-112">Cuando se entrega una licencia DRM en el equipo cliente, se coloca en el almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="54fea-112">When a DRM license is delivered to the client computer it is put into the local license store.</span></span> <span data-ttu-id="54fea-113">Se trata de un archivo protegido en el disco duro que contiene todas las licencias emitidas al usuario junto con otra información de DRM.</span><span class="sxs-lookup"><span data-stu-id="54fea-113">This is a protected file on the hard disk that contains all the licenses issued to the user along with other DRM information.</span></span>

<span data-ttu-id="54fea-114">Puede manipular los datos en el almacén de licencias local de algunas maneras limitadas mediante el uso de las API extendidas del cliente DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="54fea-114">You can manipulate data in the local license store in a few, limited ways by using the Windows Media DRM Client Extended APIs.</span></span>

<span data-ttu-id="54fea-115">Además del almacén de licencias local, algunos objetos hacen uso de un almacén de licencias temporal.</span><span class="sxs-lookup"><span data-stu-id="54fea-115">In addition to the local license store, some objects make use of a temporary license store.</span></span> <span data-ttu-id="54fea-116">Una licencia de un almacén temporal solo existe durante un breve período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="54fea-116">A license in a temporary store exists only for a short period of time.</span></span> <span data-ttu-id="54fea-117">Sin embargo, algunas licencias que comienzan en un almacén temporal se pueden guardar en el almacén de licencias local normal.</span><span class="sxs-lookup"><span data-stu-id="54fea-117">However, some licenses that begin in a temporary store can be saved to the regular local license store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54fea-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="54fea-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54fea-119">**Conceptos**</span><span class="sxs-lookup"><span data-stu-id="54fea-119">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




