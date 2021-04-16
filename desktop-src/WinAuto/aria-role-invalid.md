---
title: Error de rol de ARIA
description: Error de rol de ARIA
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- AriaRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df04ad94d68ae1e8e2e8d3352aa349834a2389fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "105685802"
---
# <a name="aria-role-error"></a><span data-ttu-id="0488d-104">Error de rol de ARIA</span><span class="sxs-lookup"><span data-stu-id="0488d-104">ARIA Role Error</span></span>

## <a name="text"></a><span data-ttu-id="0488d-105">Texto</span><span class="sxs-lookup"><span data-stu-id="0488d-105">Text</span></span>

<span data-ttu-id="0488d-106">El elemento tiene un rol WAI-ARIA no válido.</span><span class="sxs-lookup"><span data-stu-id="0488d-106">Element has invalid WAI-ARIA role.</span></span>

## <a name="type"></a><span data-ttu-id="0488d-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="0488d-107">Type</span></span>

<span data-ttu-id="0488d-108">Error</span><span class="sxs-lookup"><span data-stu-id="0488d-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="0488d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0488d-109">Description</span></span>

<span data-ttu-id="0488d-110">Este error se aplica a todos los elementos que tienen el atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) .</span><span class="sxs-lookup"><span data-stu-id="0488d-110">This error applies to all elements that have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute.</span></span> <span data-ttu-id="0488d-111">Indica que el atributo **role** no es un valor de rol de aplicaciones de Internet enriquecidas (WAI-ARIA) accesible para la iniciativa de accesibilidad web, tal como se define en la especificación WAI-ARIA.</span><span class="sxs-lookup"><span data-stu-id="0488d-111">It indicates that the **role** attribute is not a valid Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role value as defined by the WAI-ARIA specification.</span></span> <span data-ttu-id="0488d-112">Establecer un rol válido ayuda a garantizar que el elemento sea interpretado correctamente por los lectores de pantalla y otras herramientas de tecnología de asistencia.</span><span class="sxs-lookup"><span data-stu-id="0488d-112">Setting a valid role helps ensure that the element is correctly interpreted by screen readers and other assistive technology tools.</span></span>

<span data-ttu-id="0488d-113">Para corregir este error, establezca el atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) en un valor de rol WAI-ARIA válido.</span><span class="sxs-lookup"><span data-stu-id="0488d-113">To fix this error, set the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute to a valid WAI-ARIA role value.</span></span> <span data-ttu-id="0488d-114">Tenga en cuenta que los roles WAI-ARIA abstractos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="0488d-114">Note that abstract WAI-ARIA roles are not valid.</span></span>

## <a name="example"></a><span data-ttu-id="0488d-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0488d-115">Example</span></span>


```HTML
<!—The invalid role will not expose this element as a button. -->
<div role="backbutton" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >

<!—Setting the correct role will expose this as a button that can be clicked. -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



## <a name="related-topics"></a><span data-ttu-id="0488d-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0488d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0488d-117">Error de rol de contenedor de ARIA</span><span class="sxs-lookup"><span data-stu-id="0488d-117">ARIA Container Role Error</span></span>](aria-container-role.md)
</dt> </dl>

 

 




