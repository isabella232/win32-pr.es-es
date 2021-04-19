---
description: .
ms.assetid: c2094bbe-a4ca-4f30-b16e-14dced2912bc
title: Sistema de propiedades de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e96f931d37ef698339f9219a0dc8db43a6003e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696292"
---
# <a name="windows-property-system"></a><span data-ttu-id="a5274-103">Sistema de propiedades de Windows</span><span class="sxs-lookup"><span data-stu-id="a5274-103">Windows Property System</span></span>

## <a name="purpose"></a><span data-ttu-id="a5274-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="a5274-104">Purpose</span></span>

<span data-ttu-id="a5274-105">El sistema de propiedades de Windows es un sistema de lectura y escritura extensible de definiciones de datos que proporciona una manera uniforme de expresar metadatos sobre los elementos de Shell.</span><span class="sxs-lookup"><span data-stu-id="a5274-105">The Windows Property System is an extensible read/write system of data definitions that provides a uniform way of expressing metadata about Shell items.</span></span> <span data-ttu-id="a5274-106">El sistema de propiedades de Windows en Windows Vista y versiones posteriores le permite almacenar y recuperar metadatos para elementos de Shell.</span><span class="sxs-lookup"><span data-stu-id="a5274-106">The Windows Property system in Windows Vista and later enables you to store and retrieve metadata for Shell items.</span></span> <span data-ttu-id="a5274-107">Un elemento de Shell es cualquier parte única de contenido, como un archivo, una carpeta, un correo electrónico o un contacto.</span><span class="sxs-lookup"><span data-stu-id="a5274-107">A Shell item is any single piece of content, such as a file, folder, email, or contact.</span></span> <span data-ttu-id="a5274-108">Una propiedad es una parte individual de los metadatos asociados a un elemento de Shell.</span><span class="sxs-lookup"><span data-stu-id="a5274-108">A property is an individual piece of metadata associated with a Shell item.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a5274-109">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="a5274-109">Developer audience</span></span>

<span data-ttu-id="a5274-110">Antes de empezar a leer la documentación del SDK del sistema de propiedades de Windows, debe tener un conocimiento fundamental de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a5274-110">Before you start reading the Windows Property System SDK documentation, you should have a fundamental understanding of the following:</span></span>

-   <span data-ttu-id="a5274-111">Modelo de objetos componentes (COM)</span><span class="sxs-lookup"><span data-stu-id="a5274-111">Component Object Model (COM)</span></span>
-   <span data-ttu-id="a5274-112">Programación del espacio de nombres Shell</span><span class="sxs-lookup"><span data-stu-id="a5274-112">Shell Namespace programming</span></span>

<span data-ttu-id="a5274-113">Para obtener una introducción a COM, vea [conceptos básicos de com](../com/com-fundamentals.md).</span><span class="sxs-lookup"><span data-stu-id="a5274-113">For an introduction to COM, see [COM Fundamentals](../com/com-fundamentals.md).</span></span> <span data-ttu-id="a5274-114">Para obtener una introducción a la programación del espacio de nombres de Shell, vea [Introducción con el espacio de nombres del shell](../shell/namespace-intro.md).</span><span class="sxs-lookup"><span data-stu-id="a5274-114">For an introduction to Shell Namespace programming, see [Getting Started with the Shell Namespace](../shell/namespace-intro.md).</span></span>

<span data-ttu-id="a5274-115">Para los usos del sistema de propiedades de Windows, vea [información general sobre el sistema de propiedades: escenarios de desarrollo](property-system-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a5274-115">For uses of the Windows Property System, see [Property System Overview: Development Scenarios](property-system-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a5274-116">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="a5274-116">Run-time requirements</span></span>

<span data-ttu-id="a5274-117">El entorno de tiempo de ejecución admitido para usar el sistema de propiedades de Windows es Windows Vista o posterior y el kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="a5274-117">The supported run-time environment for using the Windows Property System is Windows Vista or later and the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a5274-118">Windows XP y Microsoft Windows Desktop Search (WDS) 3,0 o posterior también incluyen un subconjunto del sistema de propiedades de Windows.</span><span class="sxs-lookup"><span data-stu-id="a5274-118">Windows XP and Microsoft Windows Desktop Search (WDS) 3.0 or later also include a subset of the Windows Property System.</span></span> <span data-ttu-id="a5274-119">Para Windows 7 o la descarga del SDK de Windows Vista actualizado, consulte la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a5274-119">For the Windows 7 or updated Windows Vista SDK download, see the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a5274-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a5274-120">In this section</span></span>

-   [<span data-ttu-id="a5274-121">Información general del sistema de propiedades</span><span class="sxs-lookup"><span data-stu-id="a5274-121">Property System Overview</span></span>](property-system-overview.md)
-   [<span data-ttu-id="a5274-122">Guía del desarrollador del sistema de propiedades de Windows</span><span class="sxs-lookup"><span data-stu-id="a5274-122">Windows Property System Developer's Guide</span></span>](property-system-developer-s-guide.md)
-   [<span data-ttu-id="a5274-123">Referencia del sistema de propiedades</span><span class="sxs-lookup"><span data-stu-id="a5274-123">Property System Reference</span></span>](property-system-reference.md)
-   [<span data-ttu-id="a5274-124">Ejemplos de código del sistema de propiedades</span><span class="sxs-lookup"><span data-stu-id="a5274-124">Property System Code Samples</span></span>](property-system-code-samples.md)

 

 
