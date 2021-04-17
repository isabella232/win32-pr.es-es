---
description: Cómo crear un archivo DLL de filtro de DirectShow
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: Cómo crear un archivo DLL de filtro de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee964115e040d11ae10562b05899b2895f03d2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105651434"
---
# <a name="how-to-create-a-directshow-filter-dll"></a><span data-ttu-id="0bd2e-103">Cómo crear un archivo DLL de filtro de DirectShow</span><span class="sxs-lookup"><span data-stu-id="0bd2e-103">How to Create a DirectShow Filter DLL</span></span>

<span data-ttu-id="0bd2e-104">En este artículo se describe cómo implementar un componente como una biblioteca de vínculos dinámicos (DLL) en Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0bd2e-104">This article describes how to implement a component as a dynamic-link library (DLL) in Microsoft DirectShow.</span></span> <span data-ttu-id="0bd2e-105">Este artículo es una continuación de [cómo implementar IUnknown](how-to-implement-iunknown.md), en el que se describe cómo implementar la interfaz **IUnknown** mediante la derivación del componente de la clase base [**CUnknown**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="0bd2e-105">This article is a continuation from [How to Implement IUnknown](how-to-implement-iunknown.md), which describes how to implement the **IUnknown** interface by deriving your component from the [**CUnknown**](cunknown.md) base class.</span></span>

<span data-ttu-id="0bd2e-106">Este artículo contiene las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="0bd2e-106">This article contains the following sections.</span></span>

-   [<span data-ttu-id="0bd2e-107">Generadores de clases y plantillas de generador</span><span class="sxs-lookup"><span data-stu-id="0bd2e-107">Class Factories and Factory Templates</span></span>](class-factories-and-factory-templates.md)
-   [<span data-ttu-id="0bd2e-108">Matriz de plantillas de fábrica</span><span class="sxs-lookup"><span data-stu-id="0bd2e-108">Factory Template Array</span></span>](factory-template-array.md)
-   [<span data-ttu-id="0bd2e-109">Funciones DLL</span><span class="sxs-lookup"><span data-stu-id="0bd2e-109">DLL Functions</span></span>](dll-functions.md)

<span data-ttu-id="0bd2e-110">El registro de un filtro DirectShow (en oposición a un objeto COM genérico) requiere algunos pasos adicionales que no se describen en este artículo.</span><span class="sxs-lookup"><span data-stu-id="0bd2e-110">Registering a DirectShow filter (as opposed to a generic COM object) requires some additional steps that are not covered in this article.</span></span> <span data-ttu-id="0bd2e-111">Para obtener información sobre cómo registrar filtros, consulte [How to Register DirectShow filters](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="0bd2e-111">For information on registering filters, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bd2e-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0bd2e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bd2e-113">DirectShow y COM</span><span class="sxs-lookup"><span data-stu-id="0bd2e-113">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



