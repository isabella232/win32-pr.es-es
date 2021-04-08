---
title: Marco de trabajo de servicios de texto (marco de trabajo de servicios de texto)
description: Microsoft Windows Text Services Framework (TSF) es un servicio del sistema disponible como paquete redistribuible para Windows 2000.
ms.assetid: ecc34b2e-89e8-48a8-8a8e-442d2145fe24
ms.topic: article
ms.date: 01/14/2020
ms.openlocfilehash: 9c21cae442b5fbed62c00010a17849d1d5f27b49
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800692"
---
# <a name="text-services-framework-text-services-framework"></a><span data-ttu-id="5f95c-103">Marco de trabajo de servicios de texto (marco de trabajo de servicios de texto)</span><span class="sxs-lookup"><span data-stu-id="5f95c-103">Text Services Framework (Text Services Framework)</span></span>

## <a name="purpose"></a><span data-ttu-id="5f95c-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="5f95c-104">Purpose</span></span>

<span data-ttu-id="5f95c-105">Microsoft Windows Text Services Framework (TSF) es un servicio del sistema disponible como paquete redistribuible para Windows.</span><span class="sxs-lookup"><span data-stu-id="5f95c-105">Microsoft Windows Text Services Framework (TSF) is a system service available as a redistributable for Windows.</span></span> <span data-ttu-id="5f95c-106">TSF proporciona un marco de trabajo sencillo y escalable para la entrega de tecnologías avanzadas de entrada de texto y de lenguaje natural.</span><span class="sxs-lookup"><span data-stu-id="5f95c-106">TSF provides a simple and scalable framework for the delivery of advanced text input and natural language technologies.</span></span> <span data-ttu-id="5f95c-107">TSF puede estar habilitado en las aplicaciones o como servicio de texto TSF.</span><span class="sxs-lookup"><span data-stu-id="5f95c-107">TSF can be enabled in applications, or as a TSF text service.</span></span> <span data-ttu-id="5f95c-108">Un servicio de texto TSF proporciona compatibilidad multilingüe y proporciona servicios de texto como procesadores de teclado, reconocimiento de escritura a mano y reconocimiento de voz.</span><span class="sxs-lookup"><span data-stu-id="5f95c-108">A TSF text service provides multilingual support and delivers text services such as keyboard processors, handwriting recognition, and speech recognition.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="5f95c-109">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="5f95c-109">Where applicable</span></span>

<span data-ttu-id="5f95c-110">El marco de trabajo de servicios de texto es aplicable a equipos basados en Windows que usan servicios de texto y Windows XP o versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5f95c-110">Text Services Framework is applicable for Windows-based computers using text services and Windows XP or later versions of the operating system.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="5f95c-111">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="5f95c-111">Developer audience</span></span>

<span data-ttu-id="5f95c-112">El marco de trabajo de servicios de texto está diseñado para que lo usen los programadores del modelo de objetos componentes (COM) con los lenguajes de programación C/C++.</span><span class="sxs-lookup"><span data-stu-id="5f95c-112">Text Services Framework is designed for use by Component Object Model (COM) programmers using the C/C++ programming languages.</span></span> <span data-ttu-id="5f95c-113">Los programadores deben estar familiarizados con los servicios de texto para equipos basados en Windows.</span><span class="sxs-lookup"><span data-stu-id="5f95c-113">Programmers should be familiar with text services for Windows-based computers.</span></span> <span data-ttu-id="5f95c-114">Se recomienda el conocimiento del reconocimiento de escritura a mano, el reconocimiento de voz y la programación para la compatibilidad multilingüe.</span><span class="sxs-lookup"><span data-stu-id="5f95c-114">Knowledge of handwriting recognition, speech recognition, and programming for multilingual support is recommended.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5f95c-115">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="5f95c-115">Run-time requirements</span></span>

<span data-ttu-id="5f95c-116">Para el último redistribuible, descargue el SDK de la [plataforma Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span><span class="sxs-lookup"><span data-stu-id="5f95c-116">For the latest redistributable, download the [Windows 10 platform SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span>

<span data-ttu-id="5f95c-117">Para obtener más información sobre los requisitos de los elementos específicos de la API, consulte la sección de requisitos de la (/Windows/Win32/TSF/Text-Services-Framework-Reference) [documentación de referencia de TFS.</span><span class="sxs-lookup"><span data-stu-id="5f95c-117">For more information about the requirements of specific API elements, see the Requirements section in the ](/windows/win32/tsf/text-services-framework-reference)[TFS reference documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5f95c-118">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5f95c-118">In this section</span></span>



| <span data-ttu-id="5f95c-119">Tema</span><span class="sxs-lookup"><span data-stu-id="5f95c-119">Topic</span></span>                                                                                 | <span data-ttu-id="5f95c-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f95c-120">Description</span></span>                                                                                                      |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f95c-121">Acerca del marco de trabajo de servicios de texto</span><span class="sxs-lookup"><span data-stu-id="5f95c-121">About Text Services Framework</span></span>](about-text-services-framework.md)<br/>         | <span data-ttu-id="5f95c-122">Información general sobre el marco de trabajo de servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="5f95c-122">General information about Text Services Framework.</span></span><br/>                                                    |
| [<span data-ttu-id="5f95c-123">Usar el marco de trabajo de servicios de texto</span><span class="sxs-lookup"><span data-stu-id="5f95c-123">Using Text Services Framework</span></span>](using-text-services-framework.md)<br/>         | <span data-ttu-id="5f95c-124">Información sobre el uso de Text Services Framework.</span><span class="sxs-lookup"><span data-stu-id="5f95c-124">Information about using Text Services Framework.</span></span><br/>                                                      |
| [<span data-ttu-id="5f95c-125">Referencia de marco de trabajo de servicios de texto</span><span class="sxs-lookup"><span data-stu-id="5f95c-125">Text Services Framework Reference</span></span>](text-services-framework-reference.md)<br/> | <span data-ttu-id="5f95c-126">Documentación acerca de las interfaces, los métodos, las estructuras y otros elementos de código del marco de trabajo de servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="5f95c-126">Documentation about Text Services Framework interfaces, methods, structures, and other code elements.</span></span><br/> |
| [<span data-ttu-id="5f95c-127">Glosario</span><span class="sxs-lookup"><span data-stu-id="5f95c-127">Glossary</span></span>](glossary.md)<br/>                                                   | <span data-ttu-id="5f95c-128">Lista alfabética de términos técnicos que se usan en esta documentación.</span><span class="sxs-lookup"><span data-stu-id="5f95c-128">Alphabetical listing of technical terms used in this documentation.</span></span><br/>                                   |



 

## <a name="additional-resources"></a><span data-ttu-id="5f95c-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="5f95c-129">Additional resources</span></span>

<span data-ttu-id="5f95c-130">Qué debe saber antes de leer esta guía</span><span class="sxs-lookup"><span data-stu-id="5f95c-130">What You Should Know Before Reading This Guide</span></span>

<span data-ttu-id="5f95c-131">Para los fines de la ayuda del marco de trabajo de servicios de texto, el término "aplicación" hace referencia a una aplicación habilitada para TSF, el término "servicio de texto" hace referencia a un servicio de texto TSF y el término "administrador" hace referencia al administrador de TSF.</span><span class="sxs-lookup"><span data-stu-id="5f95c-131">For the purposes of the Text Services Framework Help, the term "application" refers to a TSF-enabled application, the term "text service" refers to a TSF text service, and the term "manager" refers to the TSF manager.</span></span> <span data-ttu-id="5f95c-132">Cada término se aplica como se indica a menos que se especifique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="5f95c-132">Each term applies as stated herein unless otherwise specified.</span></span> <span data-ttu-id="5f95c-133">Los proveedores de servicios de texto deben proporcionar firmas digitales con sus ejecutables binarios.</span><span class="sxs-lookup"><span data-stu-id="5f95c-133">Text service providers should provide digital signatures with their binary executables.</span></span>

 

 





