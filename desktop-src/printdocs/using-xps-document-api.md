---
description: En esta sección se describe cómo usar la API de documentos XPS para realizar tareas de programación.
ms.assetid: 05b3d7b6-7628-4a5f-87b7-9d51ead51c79
title: Uso de la API de documento XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8870c64bfa8fe478fb71174703c82a96e3723c53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002802"
---
# <a name="using-xps-document-api"></a><span data-ttu-id="a6688-103">Uso de la API de documento XPS</span><span class="sxs-lookup"><span data-stu-id="a6688-103">Using XPS Document API</span></span>

<span data-ttu-id="a6688-104">En esta sección se describe cómo usar la [API de documentos XPS](documents-xps.md) para realizar tareas de programación.</span><span class="sxs-lookup"><span data-stu-id="a6688-104">This section describes how to use the [XPS Document API](documents-xps.md) to perform programming tasks.</span></span>

<span data-ttu-id="a6688-105">Para obtener ejemplos de cómo usar la [API de documento XPS](documents-xps.md) en un programa, consulte la sección tareas de programación de la [API de documentos XPS](#xps-document-api-programming-tasks) .</span><span class="sxs-lookup"><span data-stu-id="a6688-105">For examples of how to use the [XPS Document API](documents-xps.md) in a program, see the [XPS Document API Programming Tasks](#xps-document-api-programming-tasks) section.</span></span>

<span data-ttu-id="a6688-106">Para obtener información acerca de cómo usar el modelo de objetos XPS y cómo lo implementa la [API de documento XPS](documents-xps.md), consulte [acerca de la API de documentos XPS](about-xps-document-api.md).</span><span class="sxs-lookup"><span data-stu-id="a6688-106">For information about how to use the XPS Object Model and how it is implemented by the [XPS Document API](documents-xps.md), see [About XPS Document API](about-xps-document-api.md).</span></span>

## <a name="getting-started-with-the-xps-document-api"></a><span data-ttu-id="a6688-107">Introducción con la API de documento XPS</span><span class="sxs-lookup"><span data-stu-id="a6688-107">Getting Started with the XPS Document API</span></span>

<span data-ttu-id="a6688-108">Antes de empezar a usar la API de documento XPS, asegúrese de que está familiarizado con los siguientes temas de programación:</span><span class="sxs-lookup"><span data-stu-id="a6688-108">Before you start using the XPS Document API, make sure that you are familiar with the following programming topics:</span></span><dl>

[<span data-ttu-id="a6688-109">Programación COM</span><span class="sxs-lookup"><span data-stu-id="a6688-109">COM Programming</span></span>](/windows/desktop/com/component-object-model--com--portal)  
[<span data-ttu-id="a6688-110">Control de errores en COM</span><span class="sxs-lookup"><span data-stu-id="a6688-110">Error Handling in COM</span></span>](/windows/desktop/com/error-handling-in-com)  
</dl>

<span data-ttu-id="a6688-111">Al usar la API de documento XPS, es posible que también desee usar las siguientes tecnologías:</span><span class="sxs-lookup"><span data-stu-id="a6688-111">When using the XPS Document API, you might also want to use the following technologies:</span></span><dl>

[<span data-ttu-id="a6688-112">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="a6688-112">DirectWrite</span></span>](/windows/desktop/DirectWrite/direct-write-portal)  
[<span data-ttu-id="a6688-113">API de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="a6688-113">XPS Print API</span></span>](./printing-with-the-xpsprint-api.md)  
[<span data-ttu-id="a6688-114">API de firma digital XPS</span><span class="sxs-lookup"><span data-stu-id="a6688-114">XPS Digital Signature API</span></span>](xps-digital-signatures.md)  
</dl>

## <a name="xps-document-api-programming-tasks"></a><span data-ttu-id="a6688-115">Tareas de programación de la API de documentos XPS</span><span class="sxs-lookup"><span data-stu-id="a6688-115">XPS Document API Programming Tasks</span></span>

<span data-ttu-id="a6688-116">En los temas de esta sección se describe cómo usar la [API de documento XPS](documents-xps.md) en un programa y se muestra cómo realizar algunas tareas de programación comunes.</span><span class="sxs-lookup"><span data-stu-id="a6688-116">The topics in this section describe how to use the [XPS Document API](documents-xps.md) in a program and demonstrate how to perform some common programming tasks.</span></span>

<span data-ttu-id="a6688-117">La API de documentos XPS usa colecciones para trabajar con grupos de interfaces.</span><span class="sxs-lookup"><span data-stu-id="a6688-117">The XPS Document API uses collections to work with groups of interfaces.</span></span> <span data-ttu-id="a6688-118">[Trabajar con las interfaces de colección de XPS OM](working-with-xps-object-model-collection-interfaces.md) describe cómo programar con estas colecciones.</span><span class="sxs-lookup"><span data-stu-id="a6688-118">[Working with XPS OM Collection Interfaces](working-with-xps-object-model-collection-interfaces.md) describes how to program with these collections.</span></span>

<span data-ttu-id="a6688-119">Entre las [tareas comunes de programación de documentos XPS](common-xps-document-tasks.md) se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="a6688-119">The [Common XPS Document Programming Tasks](common-xps-document-tasks.md) include the following:</span></span>

<dl>

[<span data-ttu-id="a6688-120">Inicializar un OM XPS</span><span class="sxs-lookup"><span data-stu-id="a6688-120">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)  
[<span data-ttu-id="a6688-121">Crear un OM XPS en blanco</span><span class="sxs-lookup"><span data-stu-id="a6688-121">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)  
[<span data-ttu-id="a6688-122">Leer un documento XPS en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="a6688-122">Read an XPS Document into an XPS OM</span></span>](read-an-xps-document-into-an-xps-om.md)  
[<span data-ttu-id="a6688-123">Navegar por el OM de XPS</span><span class="sxs-lookup"><span data-stu-id="a6688-123">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)  
[<span data-ttu-id="a6688-124">Escribir texto en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="a6688-124">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)  
[<span data-ttu-id="a6688-125">Dibujar gráficos en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="a6688-125">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)  
[<span data-ttu-id="a6688-126">Colocar imágenes en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="a6688-126">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)  
[<span data-ttu-id="a6688-127">Escribir un OM XPS en un documento XPS</span><span class="sxs-lookup"><span data-stu-id="a6688-127">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)  
[<span data-ttu-id="a6688-128">Imprimir un OM XPS</span><span class="sxs-lookup"><span data-stu-id="a6688-128">Print an XPS OM</span></span>](print-an-xps-om.md)  
  
</dl>

<span data-ttu-id="a6688-129">Entre las [tareas de programación de documentos XPS avanzadas](advanced-xps-document-tasks.md) se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="a6688-129">The [Advanced XPS Document Programming Tasks](advanced-xps-document-tasks.md) include the following:</span></span>

<dl>

[<span data-ttu-id="a6688-130">Combinar documentos XPS</span><span class="sxs-lookup"><span data-stu-id="a6688-130">Merge XPS Documents</span></span>](merging-xps-documents.md)  
[<span data-ttu-id="a6688-131">Procesar documentos XPS en un filtro XPSDrv</span><span class="sxs-lookup"><span data-stu-id="a6688-131">Processing XPS Documents in an XPSDrv Filter</span></span>](processing-xps-documents-in-an-xpsdrv-filter.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="a6688-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6688-132">Related topics</span></span>

<dl> <span data-ttu-id="a6688-133"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="a6688-133"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="a6688-134">Referencia de la API de documentos XPS</span><span class="sxs-lookup"><span data-stu-id="a6688-134">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="a6688-135">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="a6688-135">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
