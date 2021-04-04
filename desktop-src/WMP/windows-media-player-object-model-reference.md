---
title: Referencia del modelo de objetos de Windows Media Player
description: Referencia del modelo de objetos de Windows Media Player
ms.assetid: af313b94-230b-47d7-a3ad-7e23b669886f
keywords:
- Media Player de Windows, modelo de objetos
- Windows Media Player Mobile, modelo de objetos
- Modelo de objetos de Windows Media Player, referencia
- modelo de objetos, referencia
- Control ActiveX, referencia
- Control ActiveX de Windows Media Player, referencia
- Control ActiveX móvil de Windows Media Player, referencia
- referencia sobre el modelo de objetos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6128ff3f69968ddf4f8a35955907a18876ef090
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076246"
---
# <a name="windows-media-player-object-model-reference"></a><span data-ttu-id="11144-111">Referencia del modelo de objetos de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="11144-111">Windows Media Player Object Model Reference</span></span>

<span data-ttu-id="11144-112">Las secciones de referencia del modelo de objetos de Windows Media Player contienen información detallada sobre el modelo de objetos de control ActiveX de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="11144-112">The Windows Media Player Object Model Reference sections contain detailed information about the Windows Media Player ActiveX control object model.</span></span> <span data-ttu-id="11144-113">El modelo de objetos de proporciona interfaces que permiten a los desarrolladores agregar funcionalidad de Media Player de Windows a páginas web, programas de C++ y aplicaciones .NET.</span><span class="sxs-lookup"><span data-stu-id="11144-113">The object model provides interfaces that let developers add Windows Media Player functionality to webpages, C++ programs, and .NET applications.</span></span>

<span data-ttu-id="11144-114">La referencia del modelo de objetos para scripting se presenta en un estilo diseñado para su uso con lenguajes de scripts como Microsoft JScript, y documenta el modelo de objetos en términos de objetos con sus propiedades, métodos y eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="11144-114">The Object Model Reference for Scripting is presented in a style designed for use with script languages like Microsoft JScript, and it documents the object model in terms of objects with their associated properties, methods, and events.</span></span>

<span data-ttu-id="11144-115">La referencia del modelo de objetos de para C++ proporciona documentación para las interfaces COM que los programadores de C++ pueden utilizar para comunicarse con el control ActiveX de Windows Media Player o el control ActiveX de Windows Media Player Mobile.</span><span class="sxs-lookup"><span data-stu-id="11144-115">The Object Model Reference for C++ provides documentation for COM interfaces that C++ programmers can use to communicate with the Windows Media Player ActiveX control or the Windows Media Player Mobile ActiveX control.</span></span> <span data-ttu-id="11144-116">La mayoría de estas interfaces las implementa el control Media Player de Windows y la aplicación de C++ la llama.</span><span class="sxs-lookup"><span data-stu-id="11144-116">Most of these interfaces are implemented by Windows Media Player control and called by the C++ application.</span></span> <span data-ttu-id="11144-117">Sin embargo, algunas de las interfaces (por ejemplo, **IWMPEvents** y **IWMPRemoteMediaServices**) las implementa la aplicación de C++ y las llama el control Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="11144-117">However, some of the interfaces (for example, **IWMPEvents** and **IWMPRemoteMediaServices**) are implemented by the C++ application and called by the Windows Media Player control.</span></span>

<span data-ttu-id="11144-118">La referencia del modelo de objetos de Visual Basic .NET y C# proporciona documentación para las propiedades, los métodos y los eventos del objeto **AxWindowsMediaPlayer** y para las interfaces del control ActiveX de Windows Media Player que están disponibles a través de la interoperabilidad com en una solución codificada en Visual Studio .net 2002 o posterior.</span><span class="sxs-lookup"><span data-stu-id="11144-118">The Object Model Reference for Visual Basic .NET and C# provides documentation for the properties, methods, and events of the **AxWindowsMediaPlayer** object and for interfaces to the Windows Media Player ActiveX control that are available through COM interoperability in a solution coded in Visual Studio .NET 2002 or later.</span></span>

<span data-ttu-id="11144-119">La referencia del modelo de objetos de Windows Media Player contiene las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="11144-119">The Windows Media Player Object Model Reference contains the following sections.</span></span>



| <span data-ttu-id="11144-120">Sección</span><span class="sxs-lookup"><span data-stu-id="11144-120">Section</span></span>                                                                                                        | <span data-ttu-id="11144-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="11144-121">Description</span></span>                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11144-122">Referencia del modelo de objetos para scripting</span><span class="sxs-lookup"><span data-stu-id="11144-122">Object Model Reference for Scripting</span></span>](object-model-reference-for-scripting.md)                               | <span data-ttu-id="11144-123">Proporciona documentación de referencia para las propiedades, los métodos y los eventos que el modelo de objetos pone a disposición de los lenguajes de scripting.</span><span class="sxs-lookup"><span data-stu-id="11144-123">Provides reference documentation for the properties, methods, and events that the object model makes available to scripting languages.</span></span> <span data-ttu-id="11144-124">Esta información también es útil para la programación de Visual Basic 6,0.</span><span class="sxs-lookup"><span data-stu-id="11144-124">This information is also useful for Visual Basic 6.0 programming.</span></span> |
| [<span data-ttu-id="11144-125">Referencia del modelo de objetos para C++</span><span class="sxs-lookup"><span data-stu-id="11144-125">Object Model Reference for C++</span></span>](object-model-reference-for-c.md)                                             | <span data-ttu-id="11144-126">Proporciona documentación de referencia para las interfaces de C++.</span><span class="sxs-lookup"><span data-stu-id="11144-126">Provides reference documentation for C++ interfaces.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="11144-127">Referencia del modelo de objetos para Visual Basic .NET y C #</span><span class="sxs-lookup"><span data-stu-id="11144-127">Object Model Reference for Visual Basic .NET and C#</span></span>](object-model-reference-for-visual-basic--net-and-c.md) | <span data-ttu-id="11144-128">Proporciona documentación de referencia para objetos e interfaces disponibles para Visual Basic los programadores de .NET y C# a través de la interoperabilidad COM.</span><span class="sxs-lookup"><span data-stu-id="11144-128">Provides reference documentation for objects and interfaces available to Visual Basic .NET and C# programmers through COM interoperability.</span></span>                                                             |
| [<span data-ttu-id="11144-129">Referencia de atributo</span><span class="sxs-lookup"><span data-stu-id="11144-129">Attribute Reference</span></span>](attribute-reference.md)                                                                 | <span data-ttu-id="11144-130">Proporciona documentación de referencia para los atributos de metadatos que son de interés para los desarrolladores del SDK de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="11144-130">Provides reference documentation for metadata attributes that are of interest to Windows Media Player SDK developers.</span></span>                                                                                    |
| [<span data-ttu-id="11144-131">Tipos de enumeración</span><span class="sxs-lookup"><span data-stu-id="11144-131">Enumeration Types</span></span>](enumeration-types.md)                                                                     | <span data-ttu-id="11144-132">Proporciona documentación de referencia para los tipos de enumeración que utilizan las interfaces de C++ y .NET.</span><span class="sxs-lookup"><span data-stu-id="11144-132">Provides reference documentation for the enumeration types that are used by the C++ and .NET interfaces.</span></span>                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="11144-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="11144-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11144-134">**Modelo de objetos de Media Player de Windows**</span><span class="sxs-lookup"><span data-stu-id="11144-134">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 




