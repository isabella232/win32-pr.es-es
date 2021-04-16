---
title: NullParent
description: NullParent
ms.assetid: F9563D73-66EF-4C66-8783-B034AA7A212E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 765217f8d2d46645358d590c5a93310b04da01b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357017"
---
# <a name="nullparent"></a><span data-ttu-id="374e7-103">NullParent</span><span class="sxs-lookup"><span data-stu-id="374e7-103">NullParent</span></span>

## <a name="text"></a><span data-ttu-id="374e7-104">Texto</span><span class="sxs-lookup"><span data-stu-id="374e7-104">Text</span></span>

<span data-ttu-id="374e7-105">Elements Parent es NULL</span><span class="sxs-lookup"><span data-stu-id="374e7-105">Elements parent is NULL</span></span>

## <a name="type"></a><span data-ttu-id="374e7-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="374e7-106">Type</span></span>

<span data-ttu-id="374e7-107">Error</span><span class="sxs-lookup"><span data-stu-id="374e7-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="374e7-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="374e7-108">Description</span></span>

<span data-ttu-id="374e7-109">Se devuelve NULL cuando se llama a [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) en el elemento.</span><span class="sxs-lookup"><span data-stu-id="374e7-109">NULL is returned when [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the element.</span></span> <span data-ttu-id="374e7-110">El método **Get \_ accParent** debe devolver null solo cuando se llama en el elemento raíz del destino de comprobación.</span><span class="sxs-lookup"><span data-stu-id="374e7-110">The **get\_accParent** method should return NULL only when called on the root element of the verification target.</span></span>

<span data-ttu-id="374e7-111">Este problema puede provocar problemas de navegación en herramientas automatizadas, ya que el recorrido de los elementos puede ser errático e imprevisible.</span><span class="sxs-lookup"><span data-stu-id="374e7-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="374e7-112">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="374e7-112">Possible causes</span></span>

<span data-ttu-id="374e7-113">Implementación de MSAA incorrecta o no válida.</span><span class="sxs-lookup"><span data-stu-id="374e7-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="374e7-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="374e7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="374e7-115">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="374e7-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="374e7-116">**IAccessible:: get \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="374e7-116">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




