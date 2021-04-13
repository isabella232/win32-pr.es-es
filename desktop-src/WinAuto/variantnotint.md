---
title: VariantNotInt (CheckRole)
description: VariantNotInt (CheckRole)
ms.assetid: 24A9E91D-92E6-492B-B5CE-DF42E5923F60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdca744468d863ff1ab95b66edf5b3ff1f40b48f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357158"
---
# <a name="variantnotint-checkrole"></a><span data-ttu-id="94410-103">VariantNotInt (CheckRole)</span><span class="sxs-lookup"><span data-stu-id="94410-103">VariantNotInt (CheckRole)</span></span>

## <a name="text"></a><span data-ttu-id="94410-104">Texto</span><span class="sxs-lookup"><span data-stu-id="94410-104">Text</span></span>

<span data-ttu-id="94410-105">La variante devuelta de {0} debe ser una {1} pero es {2} .</span><span class="sxs-lookup"><span data-stu-id="94410-105">The variant returned from {0} should be an {1} but is a {2}.</span></span>

## <a name="type"></a><span data-ttu-id="94410-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="94410-106">Type</span></span>

<span data-ttu-id="94410-107">Error</span><span class="sxs-lookup"><span data-stu-id="94410-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="94410-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="94410-108">Description</span></span>

<span data-ttu-id="94410-109">Un elemento está informando de un rol de MSAA no válido.</span><span class="sxs-lookup"><span data-stu-id="94410-109">An element is reporting an invalid MSAA role.</span></span> <span data-ttu-id="94410-110">Por ejemplo, el método [**Get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) que se usa para recuperar el rol de MSAA de un elemento debe devolver un valor entero que represente una de las constantes de rol de MSAA, pero que devuelve otra variante en su lugar.</span><span class="sxs-lookup"><span data-stu-id="94410-110">For example, the [**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) method used to retrieve the MSAA role of an element should return an integer value that represents one of the MSAA role constants, but is returning another variant instead.</span></span>

<span data-ttu-id="94410-111">Este problema causa problemas para las personas que confían en un lector de pantalla y un teclado para la navegación, ya que los elementos se pueden identificar incorrectamente al usuario.</span><span class="sxs-lookup"><span data-stu-id="94410-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because elements may be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="94410-112">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="94410-112">Possible causes</span></span>

<span data-ttu-id="94410-113">El elemento o su elemento primario tiene un rol de MSAA establecido incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="94410-113">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94410-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="94410-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94410-115">**IAccessible:: get \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="94410-115">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="94410-116">**Roles de objeto**</span><span class="sxs-lookup"><span data-stu-id="94410-116">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




