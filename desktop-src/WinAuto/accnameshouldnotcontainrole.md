---
title: AccNameShouldNotContainRole
description: AccNameShouldNotContainRole
ms.assetid: 271461FF-5123-482F-B66D-A323CB3361DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fb91eeeb34d484c1f51cd0b7cd2d2947e86abda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779729"
---
# <a name="accnameshouldnotcontainrole"></a><span data-ttu-id="60a68-103">AccNameShouldNotContainRole</span><span class="sxs-lookup"><span data-stu-id="60a68-103">AccNameShouldNotContainRole</span></span>

## <a name="text"></a><span data-ttu-id="60a68-104">Texto</span><span class="sxs-lookup"><span data-stu-id="60a68-104">Text</span></span>

<span data-ttu-id="60a68-105">El nombre del elemento ( {0} ) no debe contener el texto del rol del elemento ( {1} )</span><span class="sxs-lookup"><span data-stu-id="60a68-105">Element's Name ({0}) should not contain the text of the Element's Role ({1})</span></span>

## <a name="type"></a><span data-ttu-id="60a68-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="60a68-106">Type</span></span>

<span data-ttu-id="60a68-107">Advertencia</span><span class="sxs-lookup"><span data-stu-id="60a68-107">Warning</span></span>

## <a name="description"></a><span data-ttu-id="60a68-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="60a68-108">Description</span></span>

<span data-ttu-id="60a68-109">El nombre de un elemento incorpora su rol de MSAA o el tipo de control UIA.</span><span class="sxs-lookup"><span data-stu-id="60a68-109">The name of an element incorporates its MSAA role or UIA control type.</span></span> <span data-ttu-id="60a68-110">Por ejemplo, esta advertencia puede producirse si el método [**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) (que se usa para recuperar el nombre de MSAA de un elemento) devuelve \_ " \_ ScrollBar System ScrollBar \_ \* ".</span><span class="sxs-lookup"><span data-stu-id="60a68-110">For example, this warning can occur if the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method—which is used to retrieve the MSAA name of an element—returns "ROLE\_SYSTEM\_SCROLLBAR\_\*".</span></span>

<span data-ttu-id="60a68-111">Este problema causa problemas para las personas que confían en un lector de pantalla y un teclado para la navegación porque el rol se leerá dos veces, o puede que no sea pronunciable o no intuitivo para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="60a68-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because the role will be read twice, or it may be unpronounceable or non-intuitive for users.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="60a68-112">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="60a68-112">Possible causes</span></span>

-   <span data-ttu-id="60a68-113">El elemento o su elemento primario tiene un nombre o una etiqueta asignados incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="60a68-113">The element or its parent has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="60a68-114">El elemento o su elemento primario tiene un nombre predeterminado que no se ha revisado en un nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="60a68-114">The element or its parent has a default name that has not been revised to a friendly name.</span></span> <span data-ttu-id="60a68-115">Por ejemplo, button1.</span><span class="sxs-lookup"><span data-stu-id="60a68-115">For example, button1.</span></span>
-   <span data-ttu-id="60a68-116">Un desarrollador no es consciente de que los lectores de pantalla leen los nombres.</span><span class="sxs-lookup"><span data-stu-id="60a68-116">A developer is not aware that screen readers read names.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60a68-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="60a68-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60a68-118">**IAccessible:: get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="60a68-118">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="60a68-119">Propiedad Name</span><span class="sxs-lookup"><span data-stu-id="60a68-119">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




