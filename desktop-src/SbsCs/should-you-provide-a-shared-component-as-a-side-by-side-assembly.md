---
description: Los proveedores de componentes compartidos deben considerar la posibilidad de que su componente esté disponible como un ensamblado en paralelo si se cumplen uno o varios de los casos siguientes.
ms.assetid: 543451cd-0608-4302-a85b-ddce79a5cfd6
title: ¿Debe proporcionar un componente compartido como ensamblado simultáneo?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733adf400ba9ce019d9f749fcd79a1a71380c9e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912501"
---
# <a name="should-you-provide-a-shared-component-as-a-side-by-side-assembly"></a><span data-ttu-id="e0648-103">¿Debe proporcionar un componente compartido como ensamblado simultáneo?</span><span class="sxs-lookup"><span data-stu-id="e0648-103">Should you provide a shared component as a side-by-side assembly?</span></span>

<span data-ttu-id="e0648-104">Los proveedores de componentes compartidos deben considerar la posibilidad de que su componente esté disponible como un ensamblado en paralelo si se cumplen una o varias de las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="e0648-104">Providers of shared components should consider making their component available as a side-by-side assembly if one or more of the following are true:</span></span>

-   <span data-ttu-id="e0648-105">El componente expone una interfaz de programación de aplicaciones enriquecida que usan muchas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e0648-105">The component exposes a rich application programming interface that is used by many applications.</span></span> <span data-ttu-id="e0648-106">Por ejemplo, un componente como MSHTML, que permite a las aplicaciones de C y C++ tener acceso al modelo de objetos de HTML dinámico (DHTML).</span><span class="sxs-lookup"><span data-stu-id="e0648-106">For example, a component such as MSHTML, which enables C and C++ applications to access the Dynamic HTML (DHTML) Object Model.</span></span>
-   <span data-ttu-id="e0648-107">El componente ya está siendo compartido por varias aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e0648-107">The component is already being shared by multiple applications.</span></span> <span data-ttu-id="e0648-108">Por ejemplo, un componente como COMCTL32, que proporciona a las aplicaciones acceso a los controles comunes.</span><span class="sxs-lookup"><span data-stu-id="e0648-108">For example, a component such as COMCTL32, which provides applications access to the common controls.</span></span>
-   <span data-ttu-id="e0648-109">El componente es un componente nuevo.</span><span class="sxs-lookup"><span data-stu-id="e0648-109">The component is a new component.</span></span>
-   <span data-ttu-id="e0648-110">El componente es un componente de modo de usuario y no un controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e0648-110">The component is a user-mode component and not a device driver.</span></span>

<span data-ttu-id="e0648-111">No todos los componentes son un candidato adecuado para un ensamblado en paralelo.</span><span class="sxs-lookup"><span data-stu-id="e0648-111">Not every component is a suitable candidate for a side-by-side assembly.</span></span> <span data-ttu-id="e0648-112">Un componente no es un candidato adecuado para un ensamblado en paralelo si se cumple alguna de las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="e0648-112">A component is not a suitable candidate for a side-by-side assembly if any of the following are true:</span></span>

-   <span data-ttu-id="e0648-113">El componente controla la comunicación entre las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e0648-113">The component handles communication between applications.</span></span> <span data-ttu-id="e0648-114">Por ejemplo, partes de OLE32 no crearía un buen ensamblado en paralelo porque no deseaba tener dos versiones diferentes de las partes que coordinan la comunicación entre las aplicaciones que se ejecutan en el sistema.</span><span class="sxs-lookup"><span data-stu-id="e0648-114">For example, parts of OLE32 would not make a good side-by-side assembly because you would not want to have two different versions of the parts that coordinate communication between applications run on your system.</span></span>
-   <span data-ttu-id="e0648-115">El componente administra un dispositivo físico o virtual para el sistema.</span><span class="sxs-lookup"><span data-stu-id="e0648-115">The component manages a physical or virtual device for the system.</span></span> <span data-ttu-id="e0648-116">Por ejemplo, un controlador de dispositivo para un administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="e0648-116">For example a device driver for a print spooler.</span></span>

<span data-ttu-id="e0648-117">En algunos casos, es posible que el desarrollador del componente rediseñe un componente existente para que sea adecuado para la publicación como un ensamblado en paralelo.</span><span class="sxs-lookup"><span data-stu-id="e0648-117">In some cases it may be possible for the developer of the component to redesign an existing component in order to make it suitable for publication as a side-by-side assembly.</span></span> <span data-ttu-id="e0648-118">Para obtener más información, consulte [instrucciones para crear ensamblados en paralelo](guidelines-for-creating-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="e0648-118">For more information see [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md).</span></span>

 

 



