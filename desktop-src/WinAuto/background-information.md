---
title: Información general
description: El componente de Microsoft Active Accessibility, oleacc.dll, crea objetos de proxy que implementan IAccessible en nombre de los controles estándar de Windows.
ms.assetid: c010af48-384c-40c0-ab52-c80b225502fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0a9b044f8035a474f02b8457dc99ec39aca73c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148777"
---
# <a name="background-information"></a><span data-ttu-id="e2b58-103">Información general</span><span class="sxs-lookup"><span data-stu-id="e2b58-103">Background Information</span></span>

<span data-ttu-id="e2b58-104">El componente de Microsoft Active Accessibility, oleacc.dll, crea objetos de proxy que implementan [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en nombre de los controles estándar de Windows.</span><span class="sxs-lookup"><span data-stu-id="e2b58-104">The Microsoft Active Accessibility component, oleacc.dll, creates proxy objects that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) on behalf of standard Windows controls.</span></span> <span data-ttu-id="e2b58-105">Dado que estos proxies usan mensajes estándar de Windows y API específicas del control para recopilar información sobre cada control, no se ha producido ningún mecanismo directo para personalizar la información que estos proxies exponen a través de **IAccessible**.</span><span class="sxs-lookup"><span data-stu-id="e2b58-105">Because these proxies use standard Windows messages and control-specific APIs to collect information about each control, there has been no direct mechanism for customizing the information these proxies expose through **IAccessible**.</span></span>

<span data-ttu-id="e2b58-106">Actualmente, puede personalizar una implementación de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) existente mediante técnicas de subclase y ajuste.</span><span class="sxs-lookup"><span data-stu-id="e2b58-106">Currently, you can customize an existing [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation using subclassing and wrapping techniques.</span></span> <span data-ttu-id="e2b58-107">Sin embargo, estas técnicas son tediosas y propensas a errores.</span><span class="sxs-lookup"><span data-stu-id="e2b58-107">However, these techniques are tedious and error-prone.</span></span> <span data-ttu-id="e2b58-108">De hecho, la mayor parte del código escrito para invalidar una o dos propiedades está relacionada con la implementación de subclases y ajuste. solo una pequeña fracción realiza la tarea real de invalidar la información.</span><span class="sxs-lookup"><span data-stu-id="e2b58-108">In fact, the majority of the code written to override one or two properties is concerned with implementing subclassing and wrapping; only a small fraction carries out the real task of overriding information.</span></span> <span data-ttu-id="e2b58-109">La anotación dinámica mejora la situación al proporcionar funcionalidades similares sin necesidad de escribir código de subestado o de ajuste.</span><span class="sxs-lookup"><span data-stu-id="e2b58-109">Dynamic Annotation improves the situation by providing similar capabilities without requiring you to write subclassing or wrapping code.</span></span> <span data-ttu-id="e2b58-110">En su lugar, puede centrarse en proporcionar código que proporcione la información correcta.</span><span class="sxs-lookup"><span data-stu-id="e2b58-110">Instead, you can focus on providing code that supplies the correct information.</span></span> <span data-ttu-id="e2b58-111">La anotación dinámica permite a los desarrolladores pasar sugerencias y otra información útil a OLEACC para personalizar la información que expone.</span><span class="sxs-lookup"><span data-stu-id="e2b58-111">Dynamic Annotation allows developers to pass hints and other useful information to OLEACC to customize the information it exposes.</span></span> <span data-ttu-id="e2b58-112">Esta capacidad solo reducirá el costo del soporte técnico de Microsoft Active Accessibility y permitirá a los desarrolladores mejorar considerablemente la accesibilidad de sus interfaces de usuario.</span><span class="sxs-lookup"><span data-stu-id="e2b58-112">This capability alone will reduce the cost of supporting Microsoft Active Accessibility and allow developers to greatly improve the accessibility of their user interfaces.</span></span>

 

 




