---
title: Instrucciones de programación de Servicios de Escritorio remoto
description: Temas que proporcionan instrucciones para desarrollar aplicaciones en un entorno de Servicios de Escritorio remoto.
ms.assetid: e0cd52c5-40d7-4a48-9d10-fdbcea46a5a0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de Servicios de Escritorio remoto, directrices de programación
- instrucciones de programación Servicios de Escritorio remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e767740a2f279c90ce4f0eb37c49919749465ad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676404"
---
# <a name="remote-desktop-services-programming-guidelines"></a><span data-ttu-id="b853f-105">Instrucciones de programación de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="b853f-105">Remote Desktop Services programming guidelines</span></span>

<span data-ttu-id="b853f-106">La mayoría de las aplicaciones basadas en Windows de 32 bits o de 64 bits se ejecutan "tal cual" en un entorno de Servicios de Escritorio remoto (conocido anteriormente como Terminal Services).</span><span class="sxs-lookup"><span data-stu-id="b853f-106">Most existing 32-bit or 64-bit Windows-based applications run "as is" in a Remote Desktop Services (formerly known as Terminal Services) environment.</span></span> <span data-ttu-id="b853f-107">Sin embargo, algunas aplicaciones funcionan correctamente y funcionan bien en un entorno de Servicios de Escritorio remoto, mientras que otras no.</span><span class="sxs-lookup"><span data-stu-id="b853f-107">However, some applications function correctly and perform well in a Remote Desktop Services environment, while others do not.</span></span> <span data-ttu-id="b853f-108">En los temas siguientes se proporcionan instrucciones para desarrollar aplicaciones en un entorno de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b853f-108">The following topics provide guidelines for developing applications in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b853f-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b853f-109">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b853f-110">Directrices para varios usuarios</span><span class="sxs-lookup"><span data-stu-id="b853f-110">Multiple-user guidelines</span></span>](multiple-user-guidelines.md)
</dt> <dd>

<span data-ttu-id="b853f-111">Directrices para desarrollar aplicaciones para varios usuarios en un entorno de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b853f-111">Guidelines for developing applications for multiple users in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="b853f-112">Instrucciones de rendimiento</span><span class="sxs-lookup"><span data-stu-id="b853f-112">Performance guidelines</span></span>](performance-guidelines.md)
</dt> <dd>

<span data-ttu-id="b853f-113">Directrices para desarrollar aplicaciones que funcionan bien en un entorno de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b853f-113">Guidelines for developing applications that perform well in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="b853f-114">Instrucciones generales de programación</span><span class="sxs-lookup"><span data-stu-id="b853f-114">General programming guidelines</span></span>](general-programming-guidelines.md)
</dt> <dd>

<span data-ttu-id="b853f-115">Directrices para desarrollar aplicaciones en un entorno de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b853f-115">Guidelines for developing applications in a Remote Desktop Services environment.</span></span>

</dd> </dl>

<span data-ttu-id="b853f-116">Muchas de estas instrucciones son buenas prácticas de programación que beneficiarán a las aplicaciones que se ejecutan en cualquier entorno de Windows.</span><span class="sxs-lookup"><span data-stu-id="b853f-116">Many of these guidelines are good programming practices that will benefit applications running in any Windows environment.</span></span> <span data-ttu-id="b853f-117">Sin embargo, algunas optimizaciones recomendadas, como la limitación de los efectos gráficos, son optimizaciones que solo deseaba cuando la aplicación se ejecuta en Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b853f-117">However, some recommended optimizations, such as limiting graphic effects, are optimizations that you would want only when your application is running under Remote Desktop Services.</span></span> <span data-ttu-id="b853f-118">Para obtener un ejemplo de código que muestra cómo detectar un entorno de Servicios de Escritorio remoto, consulte [detectar el entorno de servicios de escritorio remoto](detecting-the-terminal-services-environment.md).</span><span class="sxs-lookup"><span data-stu-id="b853f-118">For a code example that shows how to detect a Remote Desktop Services environment, see [Detecting the Remote Desktop Services Environment](detecting-the-terminal-services-environment.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b853f-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b853f-119">Related topics</span></span>

<dl> <span data-ttu-id="b853f-120"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="b853f-120"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="b853f-121">Terminal Services es ahora Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="b853f-121">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[<span data-ttu-id="b853f-122">Formato de archivo de plantilla administrativa</span><span class="sxs-lookup"><span data-stu-id="b853f-122">Administrative Template File Format</span></span>](/previous-versions/windows/desktop/Policy/administrative-template-file-format)
</dt> <dt>

[<span data-ttu-id="b853f-123">Seguridad y derechos de acceso de la clave del registro</span><span class="sxs-lookup"><span data-stu-id="b853f-123">Registry Key Security and Access Rights</span></span>](/windows/desktop/SysInfo/registry-key-security-and-access-rights)
</dt> <dt>

[<span data-ttu-id="b853f-124">Subárboles del registro</span><span class="sxs-lookup"><span data-stu-id="b853f-124">Registry Hives</span></span>](/windows/desktop/SysInfo/registry-hives)
</dt> <dt>

[<span data-ttu-id="b853f-125">Descriptor de seguridad</span><span class="sxs-lookup"><span data-stu-id="b853f-125">Security Descriptors</span></span>](/windows/desktop/SecAuthZ/security-descriptors)
</dt> <dt>

[<span data-ttu-id="b853f-126">Derechos de acceso estándar</span><span class="sxs-lookup"><span data-stu-id="b853f-126">Standard Access Rights</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[<span data-ttu-id="b853f-127">Modelo de Access Control</span><span class="sxs-lookup"><span data-stu-id="b853f-127">Access Control Model</span></span>](/windows/desktop/SecAuthZ/access-control-model)
</dt> </dl>

 

 