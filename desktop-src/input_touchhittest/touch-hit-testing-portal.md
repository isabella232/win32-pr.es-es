---
title: Prueba de posicionamiento táctil
description: En los temas de esta sección se proporciona información general sobre la compatibilidad con la prueba de posicionamiento táctil en Windows 8.
ms.assetid: bdd7630c-b2d8-4080-a149-efec018f697d
keywords:
- interacción con el usuario
- input
- puntero
- Función táctil
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 8cf6d28badb47a176a6feccf166344003faf1de8
ms.sourcegitcommit: 9e389b8e39616dcef8f7ff4bc53d945179401478
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/07/2020
ms.locfileid: "103904385"
---
# <a name="touch-hit-testing"></a><span data-ttu-id="1f6df-107">Prueba de posicionamiento táctil</span><span class="sxs-lookup"><span data-stu-id="1f6df-107">Touch Hit Testing</span></span>

## <a name="purpose"></a><span data-ttu-id="1f6df-108">Propósito</span><span class="sxs-lookup"><span data-stu-id="1f6df-108">Purpose</span></span>

<span data-ttu-id="1f6df-109">En los temas de esta sección se proporciona información general sobre la compatibilidad con la prueba de posicionamiento táctil en Windows.</span><span class="sxs-lookup"><span data-stu-id="1f6df-109">The topics in this section provide an overview of support for Touch Hit Testing in Windows.</span></span> <span data-ttu-id="1f6df-110">La prueba de posicionamiento táctil permite identificar un destino de entrada en función de si el área de contenido de un elemento de la interfaz de usuario está dentro del área de contacto o incluye el punto de contacto.</span><span class="sxs-lookup"><span data-stu-id="1f6df-110">Touch Hit Testing lets you identify an input target based on whether the content area of a UI element falls within the contact area or includes the contact point.</span></span>

<span data-ttu-id="1f6df-111">La prueba de posicionamiento táctil utiliza la geometría de contacto compleja para todo el área táctil en lugar de una única coordenada x-y.</span><span class="sxs-lookup"><span data-stu-id="1f6df-111">Touch hit testing uses complex contact geometry for the entire touch area rather than a single interpolated x-y coordinate.</span></span> <span data-ttu-id="1f6df-112">El uso de toda la geometría de contacto mejora en gran medida la precisión y precisión cuando se identifica el destino más probable de la entrada táctil.</span><span class="sxs-lookup"><span data-stu-id="1f6df-112">Using the entire contact geometry greatly improves precision and accuracy when you're identifying the most likely target of touch input.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1f6df-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="1f6df-113">In this section</span></span>

| <span data-ttu-id="1f6df-114">Tema</span><span class="sxs-lookup"><span data-stu-id="1f6df-114">Topic</span></span> | <span data-ttu-id="1f6df-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f6df-115">Description</span></span> |
| --- | --- |
| [<span data-ttu-id="1f6df-116">Referencia de la prueba de posicionamiento táctil</span><span class="sxs-lookup"><span data-stu-id="1f6df-116">Touch Hit Testing Reference</span></span>](touchhittest-reference.md)<br/> | <span data-ttu-id="1f6df-117">En los temas de esta sección se proporcionan las especificaciones de referencia para la [prueba de posicionamiento táctil](touch-hit-testing-portal.md).</span><span class="sxs-lookup"><span data-stu-id="1f6df-117">The topics in this section provide the reference specifications for [Touch Hit Testing](touch-hit-testing-portal.md).</span></span><br/> |

## <a name="developer-audience"></a><span data-ttu-id="1f6df-118">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="1f6df-118">Developer audience</span></span>

<span data-ttu-id="1f6df-119">Las API de pruebas de posicionamiento táctil están diseñadas para desarrolladores que crean marcos de interfaz de usuario que proporcionan una experiencia de usuario optimizada táctil y coherente en las aplicaciones de escritorio.</span><span class="sxs-lookup"><span data-stu-id="1f6df-119">The Touch Hit Testing APIs are designed for developers who are building UI frameworks that provide a consistent touch-optimized user experience across desktop applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f6df-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f6df-120">Related topics</span></span>

[<span data-ttu-id="1f6df-121">Interacción del usuario</span><span class="sxs-lookup"><span data-stu-id="1f6df-121">User Interaction</span></span>](../user-interaction.md)
