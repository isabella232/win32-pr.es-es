---
title: DirectWrite (DWrite)
description: Las aplicaciones actuales deben admitir la representación de texto de alta calidad, las fuentes de esquema independientes de la resolución y la compatibilidad completa con texto Unicode y diseño. DirectWrite, una API [de DirectX,](../directx.md) proporciona estas características y mucho más.
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6bdc75845c2387a4fa4335fa462d0b97ec5669
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587952"
---
# <a name="directwrite-dwrite"></a><span data-ttu-id="5919c-104">DirectWrite (DWrite)</span><span class="sxs-lookup"><span data-stu-id="5919c-104">DirectWrite (DWrite)</span></span>

## <a name="purpose"></a><span data-ttu-id="5919c-105">Propósito</span><span class="sxs-lookup"><span data-stu-id="5919c-105">Purpose</span></span>

<span data-ttu-id="5919c-106">Las aplicaciones actuales deben admitir la representación de texto de alta calidad, las fuentes de esquema independientes de la resolución y la compatibilidad completa con texto Unicode y diseño.</span><span class="sxs-lookup"><span data-stu-id="5919c-106">Today's applications must support high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support.</span></span> <span data-ttu-id="5919c-107">DirectWrite, una API [de DirectX,](../directx.md) proporciona estas características y mucho más.</span><span class="sxs-lookup"><span data-stu-id="5919c-107">DirectWrite, a [DirectX](../directx.md) API, provides these features and more.</span></span>

- <span data-ttu-id="5919c-108">Un sistema de diseño de texto independiente del dispositivo que mejora la legibilidad del texto en documentos y en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5919c-108">A device-independent text layout system that improves text readability in documents and in UI.</span></span>
- <span data-ttu-id="5919c-109">Representación de texto [ClearType](/typography/cleartype/) de Microsoft de alta calidad, sub píxeles que puede usar [GDI,](interoperating-with-gdi.md) [Direct2D](rendering-by-using-direct2d.md)o tecnología de representación específica de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5919c-109">High-quality, sub-pixel, [Microsoft ClearType](/typography/cleartype/) text rendering that can use [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md), or application-specific rendering technology.</span></span>
- <span data-ttu-id="5919c-110">Texto acelerado por hardware, cuando se usa [con Direct2D.](rendering-by-using-direct2d.md)</span><span class="sxs-lookup"><span data-stu-id="5919c-110">Hardware-accelerated text, when used with [Direct2D](rendering-by-using-direct2d.md).</span></span>
- <span data-ttu-id="5919c-111">Compatibilidad con texto con varios formatos.</span><span class="sxs-lookup"><span data-stu-id="5919c-111">Support for multi-format text.</span></span>
- <span data-ttu-id="5919c-112">Compatibilidad con las características de tipografía avanzadas de las fuentes OpenType.</span><span class="sxs-lookup"><span data-stu-id="5919c-112">Support for the advanced typography features of OpenType fonts.</span></span>
- <span data-ttu-id="5919c-113">Compatibilidad con el diseño y la representación de texto en todos los idiomas admitidos.</span><span class="sxs-lookup"><span data-stu-id="5919c-113">Support for the layout and rendering of text in all supported languages.</span></span>
- <span data-ttu-id="5919c-114">Diseño y representación compatibles con [GDI.](interoperating-with-gdi.md)</span><span class="sxs-lookup"><span data-stu-id="5919c-114">[GDI](interoperating-with-gdi.md)-compatible layout and rendering.</span></span>

<span data-ttu-id="5919c-115">La API admite la medición, el dibujo y las pruebas de acceso del texto de varios formatos.</span><span class="sxs-lookup"><span data-stu-id="5919c-115">The API supports measuring, drawing, and hit-testing of multi-format text.</span></span> <span data-ttu-id="5919c-116">DirectWrite controla el texto en todos los idiomas admitidos para aplicaciones globales y localizadas, a partir de la infraestructura de lenguaje clave que se encuentra en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5919c-116">DirectWrite handles text in all supported languages for global and localized applications, building on the key language infrastructure found in Windows 7.</span></span> <span data-ttu-id="5919c-117">DirectWrite también ofrece una API de representación de glifos de bajo nivel para los desarrolladores que quieren realizar su propio diseño y procesamiento de Unicode a glifo.</span><span class="sxs-lookup"><span data-stu-id="5919c-117">DirectWrite also provides a low-level glyph rendering API for developers who want to perform their own layout and Unicode-to-glyph processing.</span></span>

> [!NOTE]
> <span data-ttu-id="5919c-118">[El SDK](/windows/apps/windows-app-sdk/) para aplicaciones de Windows presenta una nueva versión de DirectWrite denominada DWriteCore que se ejecuta en versiones de Windows hasta Windows 8 y abre la puerta para que la use &mdash; entre plataformas. &mdash;</span><span class="sxs-lookup"><span data-stu-id="5919c-118">[Windows App SDK](/windows/apps/windows-app-sdk/) introduces a new version of DirectWrite&mdash;called DWriteCore&mdash;that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="5919c-119">Para obtener más información, vea [Introducción a DWriteCore.](dwritecore-overview.md)</span><span class="sxs-lookup"><span data-stu-id="5919c-119">For more details, see [DWriteCore overview](dwritecore-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5919c-120">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="5919c-120">Run-time requirements</span></span>

- <span data-ttu-id="5919c-121">Windows 7 o Windows Vista con Service Pack 2 (SP2) y actualización de plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5919c-121">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista</span></span>
- <span data-ttu-id="5919c-122">Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) y Platform Update para Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5919c-122">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5919c-123">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5919c-123">In this section</span></span>

| <span data-ttu-id="5919c-124">Tema</span><span class="sxs-lookup"><span data-stu-id="5919c-124">Topic</span></span> | <span data-ttu-id="5919c-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="5919c-125">Description</span></span> |
|-|-|
| [<span data-ttu-id="5919c-126">Novedades de DirectWrite</span><span class="sxs-lookup"><span data-stu-id="5919c-126">What's new in DirectWrite</span></span>](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="5919c-127">Estas son algunas de las nuevas adiciones a DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="5919c-127">Here are some of the new additions to DirectWrite.</span></span> <br/> |
| [<span data-ttu-id="5919c-128">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="5919c-128">Programming Guide</span></span>](programming-guide.md)<br/> | <span data-ttu-id="5919c-129">En los temas siguientes se proporciona información general sobre DirectWrite API.</span><span class="sxs-lookup"><span data-stu-id="5919c-129">The following topics provide an overview of the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="5919c-130">Referencia de API</span><span class="sxs-lookup"><span data-stu-id="5919c-130">API Reference</span></span>](reference.md)<br/> | <span data-ttu-id="5919c-131">Describe directWrite API.</span><span class="sxs-lookup"><span data-stu-id="5919c-131">Describes the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="5919c-132">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="5919c-132">Sample Code</span></span>](samples.md)<br/> | <span data-ttu-id="5919c-133">Esta sección contiene información sobre programas de ejemplo para DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="5919c-133">This section contains information about sample programs for DirectWrite.</span></span><br/> |
