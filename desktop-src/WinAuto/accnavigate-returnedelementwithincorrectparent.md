---
title: AccNavigate_ReturnedElementWithIncorrectParent
description: AccNavigate \_ ReturnedElementWithIncorrectParent
ms.assetid: 44447E47-04D5-4784-B5E9-E8C62A9834CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3bdff54c9c594cde4e6e57fe1886a900c913eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104559165"
---
# <a name="accnavigate_returnedelementwithincorrectparent"></a><span data-ttu-id="22322-103">AccNavigate \_ ReturnedElementWithIncorrectParent</span><span class="sxs-lookup"><span data-stu-id="22322-103">AccNavigate\_ReturnedElementWithIncorrectParent</span></span>

## <a name="text"></a><span data-ttu-id="22322-104">Texto</span><span class="sxs-lookup"><span data-stu-id="22322-104">Text</span></span>

<span data-ttu-id="22322-105">La llamada a accNavigate ((Live Search), 0, NAVDIR \_ FIRSTCHILD) que devolvió (x-gadget:///gadget.html) devolvió el elemento primario incorrecto ( \[ null \] ) y no (Live Search)</span><span class="sxs-lookup"><span data-stu-id="22322-105">Calling accNavigate((Live Search), 0, NAVDIR\_FIRSTCHILD) which returned (x-gadget:///gadget.html) returned the incorrect parent(\[NULL\]) and not (Live Search)</span></span>

## <a name="type"></a><span data-ttu-id="22322-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="22322-106">Type</span></span>

<span data-ttu-id="22322-107">Error</span><span class="sxs-lookup"><span data-stu-id="22322-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="22322-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="22322-108">Description</span></span>

<span data-ttu-id="22322-109">Cuando se llama a [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) en el elemento secundario devuelto por [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (mediante las \_ constantes de navegación NAVDIR FIRSTCHILD o NAVDIR \_ LASTCHILD), el elemento primario devuelto no coincide con el elemento primario especificado en la llamada **accNavigate** .</span><span class="sxs-lookup"><span data-stu-id="22322-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the child element returned by [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (using either the NAVDIR\_FIRSTCHILD or NAVDIR\_LASTCHILD navigation constants), the parent element returned does not match the parent element specified in the **accNavigate** call.</span></span>

![ejemplo de una implementación de MSAA no válida que devuelve un elemento primario incorrecto.](images/accchecker-invalid-msaa-parent.png)

<span data-ttu-id="22322-111">Este problema puede provocar problemas de navegación en herramientas automatizadas, ya que el recorrido de los elementos puede ser errático e imprevisible.</span><span class="sxs-lookup"><span data-stu-id="22322-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="22322-112">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="22322-112">Possible causes</span></span>

<span data-ttu-id="22322-113">Implementación de MSAA incorrecta o no válida.</span><span class="sxs-lookup"><span data-stu-id="22322-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22322-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22322-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22322-115">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="22322-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="22322-116">**IAccessible:: get \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="22322-116">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




