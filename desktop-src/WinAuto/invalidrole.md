---
title: InvalidRole
description: InvalidRole
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531aa9917bd68b615c2cd2457d7a24bfc4af336c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714135"
---
# <a name="invalidrole"></a><span data-ttu-id="aa321-103">InvalidRole</span><span class="sxs-lookup"><span data-stu-id="aa321-103">InvalidRole</span></span>

## <a name="text"></a><span data-ttu-id="aa321-104">Texto</span><span class="sxs-lookup"><span data-stu-id="aa321-104">Text</span></span>

<span data-ttu-id="aa321-105">El valor int devuelto de Get \_ accRole no es una constante de rol válida, el sistema de roles de IE \_\_\*</span><span class="sxs-lookup"><span data-stu-id="aa321-105">The int returned from get\_accRole is not a valid role constant, ie ROLE\_SYSTEM\_\*</span></span>

## <a name="type"></a><span data-ttu-id="aa321-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa321-106">Type</span></span>

<span data-ttu-id="aa321-107">Error</span><span class="sxs-lookup"><span data-stu-id="aa321-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="aa321-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa321-108">Description</span></span>

<span data-ttu-id="aa321-109">Un elemento está informando de un rol de MSAA no válido.</span><span class="sxs-lookup"><span data-stu-id="aa321-109">An element is reporting an invalid MSAA role.</span></span> <span data-ttu-id="aa321-110">Por ejemplo, el método [**Get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) devuelve un valor entero que no se asigna a una constante de rol de objeto válida (como el \_ sistema de rol \_ ListItem).</span><span class="sxs-lookup"><span data-stu-id="aa321-110">For example, the [**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) method returns an integer value that does not map to a valid object role constant (such as ROLE\_SYSTEM\_LISTITEM).</span></span>

<span data-ttu-id="aa321-111">Este problema causa problemas para las personas que confían en un lector de pantalla y un teclado para la navegación, ya que los elementos se pueden identificar incorrectamente al usuario.</span><span class="sxs-lookup"><span data-stu-id="aa321-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because elements may be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="aa321-112">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="aa321-112">Possible causes</span></span>

<span data-ttu-id="aa321-113">El elemento o su elemento primario tiene un rol de MSAA establecido incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="aa321-113">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa321-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aa321-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa321-115">**IAccessible:: get \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="aa321-115">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="aa321-116">**Roles de objeto**</span><span class="sxs-lookup"><span data-stu-id="aa321-116">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




