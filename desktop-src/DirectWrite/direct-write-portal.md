---
title: DirectWrite (DWrite)
description: Las aplicaciones actuales deben admitir la representación de texto de alta calidad, las fuentes de esquema independientes de la resolución y la compatibilidad con el diseño y el texto Unicode completo. DirectWrite, una API de [DirectX](../directx.md) , proporciona estas características y mucho más.
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b1e2ff44083a56a7202847fc07ad9daaa67b7ba
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2020
ms.locfileid: "104488908"
---
# <a name="directwrite-dwrite"></a><span data-ttu-id="903bb-104">DirectWrite (DWrite)</span><span class="sxs-lookup"><span data-stu-id="903bb-104">DirectWrite (DWrite)</span></span>

## <a name="purpose"></a><span data-ttu-id="903bb-105">Propósito</span><span class="sxs-lookup"><span data-stu-id="903bb-105">Purpose</span></span>

<span data-ttu-id="903bb-106">Las aplicaciones actuales deben admitir la representación de texto de alta calidad, las fuentes de esquema independientes de la resolución y la compatibilidad con el diseño y el texto Unicode completo.</span><span class="sxs-lookup"><span data-stu-id="903bb-106">Today's applications must support high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support.</span></span> <span data-ttu-id="903bb-107">DirectWrite, una API de [DirectX](../directx.md) , proporciona estas características y mucho más.</span><span class="sxs-lookup"><span data-stu-id="903bb-107">DirectWrite, a [DirectX](../directx.md) API, provides these features and more.</span></span>

- <span data-ttu-id="903bb-108">Sistema de diseño de texto independiente del dispositivo que mejora la legibilidad del texto en documentos y en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="903bb-108">A device-independent text layout system that improves text readability in documents and in UI.</span></span>
- <span data-ttu-id="903bb-109">Representación de texto de alta calidad, subpíxel, [ClearType de Microsoft](/typography/cleartype/) que puede usar la tecnología de representación de [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md)o específica de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="903bb-109">High-quality, sub-pixel, [Microsoft ClearType](/typography/cleartype/) text rendering that can use [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md), or application-specific rendering technology.</span></span>
- <span data-ttu-id="903bb-110">Texto con aceleración de hardware, cuando se usa con [Direct2D](rendering-by-using-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="903bb-110">Hardware-accelerated text, when used with [Direct2D](rendering-by-using-direct2d.md).</span></span>
- <span data-ttu-id="903bb-111">Compatibilidad con texto con varios formatos.</span><span class="sxs-lookup"><span data-stu-id="903bb-111">Support for multi-format text.</span></span>
- <span data-ttu-id="903bb-112">Compatibilidad con las características tipográficas avanzadas de las fuentes OpenType.</span><span class="sxs-lookup"><span data-stu-id="903bb-112">Support for the advanced typography features of OpenType fonts.</span></span>
- <span data-ttu-id="903bb-113">Compatibilidad con el diseño y la representación de texto en todos los idiomas admitidos.</span><span class="sxs-lookup"><span data-stu-id="903bb-113">Support for the layout and rendering of text in all supported languages.</span></span>
- <span data-ttu-id="903bb-114">Diseño y representación compatibles con [GDI](interoperating-with-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="903bb-114">[GDI](interoperating-with-gdi.md)-compatible layout and rendering.</span></span>

<span data-ttu-id="903bb-115">La API admite la medición, el dibujo y la prueba de posicionamiento de texto multiformato.</span><span class="sxs-lookup"><span data-stu-id="903bb-115">The API supports measuring, drawing, and hit-testing of multi-format text.</span></span> <span data-ttu-id="903bb-116">DirectWrite controla el texto en todos los idiomas admitidos para las aplicaciones globales y localizadas, y se basa en la infraestructura de idioma clave que se encuentra en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="903bb-116">DirectWrite handles text in all supported languages for global and localized applications, building on the key language infrastructure found in Windows 7.</span></span> <span data-ttu-id="903bb-117">DirectWrite también ofrece una API de representación de glifos de bajo nivel para los desarrolladores que quieren realizar su propio diseño y procesamiento de Unicode a glifo.</span><span class="sxs-lookup"><span data-stu-id="903bb-117">DirectWrite also provides a low-level glyph rendering API for developers who want to perform their own layout and Unicode-to-glyph processing.</span></span>

> [!NOTE]
> <span data-ttu-id="903bb-118">[Project reunion](/windows/apps/project-reunion/) presenta una nueva versión de DirectWrite &mdash; llamada DWriteCore &mdash; que se ejecuta en versiones de Windows hasta Windows 8 y abre la puerta para que la use entre plataformas.</span><span class="sxs-lookup"><span data-stu-id="903bb-118">[Project Reunion](/windows/apps/project-reunion/) introduces a new version of DirectWrite&mdash;called DWriteCore&mdash;that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="903bb-119">Para obtener más información, consulte [información general de DWriteCore](dwritecore-overview.md).</span><span class="sxs-lookup"><span data-stu-id="903bb-119">For more details, see [DWriteCore overview](dwritecore-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="903bb-120">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="903bb-120">Run-time requirements</span></span>

- <span data-ttu-id="903bb-121">Windows 7 o Windows Vista con Service Pack 2 (SP2) y la actualización de la plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="903bb-121">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista</span></span>
- <span data-ttu-id="903bb-122">Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) y la actualización de la plataforma para Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="903bb-122">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008</span></span>

## <a name="in-this-section"></a><span data-ttu-id="903bb-123">En esta sección</span><span class="sxs-lookup"><span data-stu-id="903bb-123">In this section</span></span>

| <span data-ttu-id="903bb-124">Tema</span><span class="sxs-lookup"><span data-stu-id="903bb-124">Topic</span></span> | <span data-ttu-id="903bb-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="903bb-125">Description</span></span> |
|-|-|
| [<span data-ttu-id="903bb-126">Novedades de DirectWrite</span><span class="sxs-lookup"><span data-stu-id="903bb-126">What's new in DirectWrite</span></span>](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="903bb-127">Estas son algunas de las nuevas adiciones a DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="903bb-127">Here are some of the new additions to DirectWrite.</span></span> <br/> |
| [<span data-ttu-id="903bb-128">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="903bb-128">Programming Guide</span></span>](programming-guide.md)<br/> | <span data-ttu-id="903bb-129">En los temas siguientes se proporciona información general sobre la API de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="903bb-129">The following topics provide an overview of the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="903bb-130">Referencia de API</span><span class="sxs-lookup"><span data-stu-id="903bb-130">API Reference</span></span>](reference.md)<br/> | <span data-ttu-id="903bb-131">Describe la API de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="903bb-131">Describes the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="903bb-132">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="903bb-132">Sample Code</span></span>](samples.md)<br/> | <span data-ttu-id="903bb-133">Esta sección contiene información sobre los programas de ejemplo de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="903bb-133">This section contains information about sample programs for DirectWrite.</span></span><br/> |
