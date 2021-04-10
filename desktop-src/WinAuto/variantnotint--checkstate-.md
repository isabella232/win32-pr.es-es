---
title: VariantNotInt (CheckState)
description: VariantNotInt (CheckState)
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d951a51ae6aa3f4d9454fc95a56c76cfe30500c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268786"
---
# <a name="variantnotint-checkstate"></a><span data-ttu-id="24e9e-103">VariantNotInt (CheckState)</span><span class="sxs-lookup"><span data-stu-id="24e9e-103">VariantNotInt (CheckState)</span></span>

## <a name="text"></a><span data-ttu-id="24e9e-104">Texto</span><span class="sxs-lookup"><span data-stu-id="24e9e-104">Text</span></span>

<span data-ttu-id="24e9e-105">La variante devuelta de {0} debe ser una {1} pero es {2} .</span><span class="sxs-lookup"><span data-stu-id="24e9e-105">The variant returned from {0} should be an {1} but is a {2}.</span></span>

## <a name="type"></a><span data-ttu-id="24e9e-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="24e9e-106">Type</span></span>

<span data-ttu-id="24e9e-107">Error</span><span class="sxs-lookup"><span data-stu-id="24e9e-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="24e9e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="24e9e-108">Description</span></span>

<span data-ttu-id="24e9e-109">Un elemento está informando de un estado de MSAA no válido.</span><span class="sxs-lookup"><span data-stu-id="24e9e-109">An element is reporting an invalid MSAA state.</span></span> <span data-ttu-id="24e9e-110">Por ejemplo, el método [**Get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) que se usa para recuperar el estado de MSAA de un elemento debe devolver un valor entero que represente una de las constantes de estado de MSAA, pero que devuelve otra variante en su lugar.</span><span class="sxs-lookup"><span data-stu-id="24e9e-110">For example, the [**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) method used to retrieve the MSAA state of an element should return an integer value that represents one of the MSAA state constants, but is returning another variant instead.</span></span>

<span data-ttu-id="24e9e-111">Este problema causa problemas para las personas que confían en un lector de pantalla y un teclado para la navegación porque es posible que se notifique al usuario un estado incorrecto del elemento.</span><span class="sxs-lookup"><span data-stu-id="24e9e-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an incorrect element state might be reported to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="24e9e-112">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="24e9e-112">Possible causes</span></span>

<span data-ttu-id="24e9e-113">El elemento o su elemento primario tiene un estado de MSAA establecido incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="24e9e-113">The element or its parent has an MSAA state set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24e9e-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="24e9e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24e9e-115">**IAccessible:: get \_ accState**</span><span class="sxs-lookup"><span data-stu-id="24e9e-115">**IAccessible::get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[<span data-ttu-id="24e9e-116">**Constantes de estado de objeto**</span><span class="sxs-lookup"><span data-stu-id="24e9e-116">**Object State Constants**</span></span>](object-state-constants.md)
</dt> </dl>

 

 




