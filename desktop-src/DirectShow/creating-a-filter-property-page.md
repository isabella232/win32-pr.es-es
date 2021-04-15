---
description: Crear una página de propiedades de filtro
ms.assetid: 028e2c4e-0241-4057-8514-d3e9b456ab6e
title: Crear una página de propiedades de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cc19bf918ba47c53a04e34f5e5292bfdc716eca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666119"
---
# <a name="creating-a-filter-property-page"></a><span data-ttu-id="d369d-103">Crear una página de propiedades de filtro</span><span class="sxs-lookup"><span data-stu-id="d369d-103">Creating a Filter Property Page</span></span>

<span data-ttu-id="d369d-104">En esta sección se describe cómo crear una página de propiedades para un filtro DirectShow personalizado mediante la clase [**CBasePropertyPage**](cbasepropertypage.md) .</span><span class="sxs-lookup"><span data-stu-id="d369d-104">This section describes how to create a property page for a custom DirectShow filter, using the [**CBasePropertyPage**](cbasepropertypage.md) class.</span></span> <span data-ttu-id="d369d-105">En el código de ejemplo de esta sección se muestran todos los pasos necesarios para crear una página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d369d-105">The example code in this section shows all the steps needed to create a property page.</span></span> <span data-ttu-id="d369d-106">En el ejemplo se muestra una página de propiedades para un filtro hipotético de efecto de vídeo que admite una propiedad de saturación.</span><span class="sxs-lookup"><span data-stu-id="d369d-106">The example shows a property page for a hypothetical video effect filter that supports a saturation property.</span></span> <span data-ttu-id="d369d-107">La página de propiedades tiene un control deslizante, que el usuario puede desplazar para ajustar el nivel de saturación del filtro.</span><span class="sxs-lookup"><span data-stu-id="d369d-107">The property page has a slider, which the user can move to adjust the filter's saturation level.</span></span>

<span data-ttu-id="d369d-108">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="d369d-108">This section contains the following topics:</span></span>

-   [<span data-ttu-id="d369d-109">Paso 1. Definir un mecanismo para establecer la propiedad</span><span class="sxs-lookup"><span data-stu-id="d369d-109">Step 1. Define a Mechanism for Setting the Property</span></span>](step-1--define-a-mechanism-for-setting-the-property.md)
-   [<span data-ttu-id="d369d-110">Paso 2. Implementar ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="d369d-110">Step 2. Implement ISpecifyPropertyPages</span></span>](step-2--implement-ispecifypropertypages.md)
-   [<span data-ttu-id="d369d-111">Paso 3. Compatibilidad con QueryInterface</span><span class="sxs-lookup"><span data-stu-id="d369d-111">Step 3. Support QueryInterface</span></span>](step-3--support-queryinterface.md)
-   [<span data-ttu-id="d369d-112">Paso 4. Crear la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="d369d-112">Step 4. Create the Property Page</span></span>](step-4--create-the-property-page.md)
-   [<span data-ttu-id="d369d-113">Paso 5. Almacenar un puntero al filtro</span><span class="sxs-lookup"><span data-stu-id="d369d-113">Step 5. Store a Pointer to the Filter</span></span>](step-5--store-a-pointer-to-the-filter.md)
-   [<span data-ttu-id="d369d-114">Paso 6. Inicializar el cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="d369d-114">Step 6. Initialize the Dialog</span></span>](step-6--initialize-the-dialog.md)
-   [<span data-ttu-id="d369d-115">Paso 7. Controlar mensajes de ventana</span><span class="sxs-lookup"><span data-stu-id="d369d-115">Step 7. Handle Window Messages</span></span>](step-7--handle-window-messages.md)
-   [<span data-ttu-id="d369d-116">Paso 8. Aplicar cambios de propiedad</span><span class="sxs-lookup"><span data-stu-id="d369d-116">Step 8. Apply Property Changes</span></span>](step-8--apply-property-changes.md)
-   [<span data-ttu-id="d369d-117">Paso 9. Desconectar la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="d369d-117">Step 9. Disconnect the Property Page</span></span>](step-9--disconnect-the-property-page.md)
-   [<span data-ttu-id="d369d-118">Paso 10. Compatibilidad con el registro COM</span><span class="sxs-lookup"><span data-stu-id="d369d-118">Step 10. Support COM Registration</span></span>](step-10--support-com-registration.md)

## <a name="related-topics"></a><span data-ttu-id="d369d-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d369d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d369d-120">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="d369d-120">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



