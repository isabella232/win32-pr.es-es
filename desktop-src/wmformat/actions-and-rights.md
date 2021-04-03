---
title: Acciones y derechos
description: Acciones y derechos
ms.assetid: 711c6a04-6c40-4ea5-8c4f-91d000286b7b
keywords:
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- SDK de Windows Media Format, licencias de DRM
- SDK de Windows Media Format, licencias de DRM
- Administración de derechos digitales (DRM), acciones
- DRM (administración de derechos digitales), acciones
- Administración de derechos digitales (DRM), derechos
- DRM (administración de derechos digitales), derechos
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- licencias, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d044850bb5ee73e804065c67840362ec0b7b0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075190"
---
# <a name="actions-and-rights"></a><span data-ttu-id="8d22a-113">Acciones y derechos</span><span class="sxs-lookup"><span data-stu-id="8d22a-113">Actions and Rights</span></span>

<span data-ttu-id="8d22a-114">Cuando un archivo está protegido mediante DRM de Windows Media, su uso está completamente restringido.</span><span class="sxs-lookup"><span data-stu-id="8d22a-114">When a file is protected by using Windows Media DRM, its use is completely restricted.</span></span> <span data-ttu-id="8d22a-115">Se pueden emitir licencias para permitir que los usuarios usen el contenido de maneras específicas.</span><span class="sxs-lookup"><span data-stu-id="8d22a-115">Licenses can be issued to enable a user to use the content in specific ways.</span></span> <span data-ttu-id="8d22a-116">Cada una de las formas en que un usuario puede usar el contenido se describe mediante una acción.</span><span class="sxs-lookup"><span data-stu-id="8d22a-116">Each way in which a user might use the content is described by an action.</span></span> <span data-ttu-id="8d22a-117">Por ejemplo, la reproducción de un archivo en un equipo es una acción.</span><span class="sxs-lookup"><span data-stu-id="8d22a-117">For example, playing a file on a computer is an action.</span></span>

<span data-ttu-id="8d22a-118">Se dice que una licencia que habilita una determinada acción concede un derecho.</span><span class="sxs-lookup"><span data-stu-id="8d22a-118">A license that enables a given action is said to grant a right.</span></span> <span data-ttu-id="8d22a-119">Por ejemplo, una licencia puede conceder el derecho a reproducir contenido en un equipo.</span><span class="sxs-lookup"><span data-stu-id="8d22a-119">For example, a license can grant the right to play content on a computer.</span></span>

<span data-ttu-id="8d22a-120">Las acciones y los derechos hacen referencia a las mismas maneras de usar el contenido.</span><span class="sxs-lookup"><span data-stu-id="8d22a-120">Actions and rights refer to the same ways of using content.</span></span> <span data-ttu-id="8d22a-121">La diferencia es que la acción hace referencia al uso mientras el derecho hace referencia al permiso.</span><span class="sxs-lookup"><span data-stu-id="8d22a-121">The difference is that the action refers to the use while the right refers to the permission.</span></span> <span data-ttu-id="8d22a-122">A pesar de esta distinción, las palabras acción y derecha se usan a menudo indistintamente en esta documentación y en otros documentos que describen Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="8d22a-122">Despite this distinction, the words action and right are often used interchangeably in this documentation and in other documents that describe Windows Media DRM.</span></span>

<span data-ttu-id="8d22a-123">Las acciones controladas por los derechos de DRM de Windows Media se enumeran en la sección de [constantes derechos](rights-constants.md) de esta documentación.</span><span class="sxs-lookup"><span data-stu-id="8d22a-123">The actions governed by Windows Media DRM rights are listed in the [Rights Constants](rights-constants.md) section of this documentation.</span></span>

<span data-ttu-id="8d22a-124">Ciertos métodos de las API extendidas del cliente DRM de Windows Media usan diferentes constantes para hacer referencia a los derechos básicos de DRM.</span><span class="sxs-lookup"><span data-stu-id="8d22a-124">Certain methods of the Windows Media DRM Client Extended APIs use different constants to refer to the basic DRM rights.</span></span> <span data-ttu-id="8d22a-125">Por ejemplo, el método [**IWMDRMLicenseQuery:: QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) usa un conjunto de cadenas específicas de los Estados de licencia.</span><span class="sxs-lookup"><span data-stu-id="8d22a-125">For example, the [**IWMDRMLicenseQuery::QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) method uses a set of strings specific to license states.</span></span> <span data-ttu-id="8d22a-126">Aunque estas constantes definen cadenas diferentes de las constantes de derechos básicas, hacen referencia a los mismos derechos de la licencia.</span><span class="sxs-lookup"><span data-stu-id="8d22a-126">Even though these constants are defining different strings than the basic rights constants, they refer to the same rights in the license.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d22a-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8d22a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d22a-128">**Conceptos**</span><span class="sxs-lookup"><span data-stu-id="8d22a-128">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




