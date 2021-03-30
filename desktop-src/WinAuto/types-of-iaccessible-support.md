---
title: Tipos de compatibilidad de IAccessible
description: Tipos de compatibilidad de IAccessible
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb2cb3d25e4cf95cc1ad790c77ffe66e02efda2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776224"
---
# <a name="types-of-iaccessible-support"></a><span data-ttu-id="ec07e-103">Tipos de compatibilidad de IAccessible</span><span class="sxs-lookup"><span data-stu-id="ec07e-103">Types of IAccessible Support</span></span>

<span data-ttu-id="ec07e-104">Los servidores de Microsoft Active Accessibility tienen dos tipos de compatibilidad con [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : nativo y proxy.</span><span class="sxs-lookup"><span data-stu-id="ec07e-104">Microsoft Active Accessibility servers have two types of [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support: native and proxied.</span></span> <span data-ttu-id="ec07e-105">Los elementos de la interfaz de usuario usados en una aplicación determinan qué tipo de soporte técnico es adecuado.</span><span class="sxs-lookup"><span data-stu-id="ec07e-105">The UI elements used in an application determine which type of support is appropriate.</span></span> <span data-ttu-id="ec07e-106">Muchos servidores que se escriben actualmente sacan el máximo partido de los proxies de **IAccessible** y solo implementan **IAccessible** para los controles que no son proxy de Oleacc.dll, como controles sin ventanas o controles con un nombre de clase de ventana personalizado.</span><span class="sxs-lookup"><span data-stu-id="ec07e-106">Many servers being written today take full advantage of **IAccessible** proxies and only implement **IAccessible** for those controls that are not proxied by Oleacc.dll, such as windowless controls or controls with a custom window class name.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ec07e-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ec07e-107">In this section</span></span>

-   [<span data-ttu-id="ec07e-108">Implementación de Active Accessibility nativa</span><span class="sxs-lookup"><span data-stu-id="ec07e-108">Native Active Accessibility Implementation</span></span>](native-active-accessibility-implementation.md)
-   [<span data-ttu-id="ec07e-109">Proxies de IAccessible</span><span class="sxs-lookup"><span data-stu-id="ec07e-109">IAccessible Proxies</span></span>](iaccessible-proxies.md)

 

 




