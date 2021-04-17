---
description: MFTrace es una herramienta para generar registros de seguimiento para aplicaciones Media Foundation.
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a216f225141ceccf3f1357025dd069afa494d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653383"
---
# <a name="mftrace"></a><span data-ttu-id="4c7e7-103">MFTrace</span><span class="sxs-lookup"><span data-stu-id="4c7e7-103">MFTrace</span></span>

<span data-ttu-id="4c7e7-104">MFTrace es una herramienta para generar registros de seguimiento para aplicaciones Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="4c7e7-104">MFTrace is a tool for generating trace logs for Media Foundation applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4c7e7-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="4c7e7-105">In this section</span></span>

-   [<span data-ttu-id="4c7e7-106">Usar MFTrace</span><span class="sxs-lookup"><span data-stu-id="4c7e7-106">Using MFTrace</span></span>](using-mftrace.md)
-   [<span data-ttu-id="4c7e7-107">Palabras clave de MFTrace</span><span class="sxs-lookup"><span data-stu-id="4c7e7-107">MFTrace Keywords</span></span>](mftrace-keywords.md)
-   [<span data-ttu-id="4c7e7-108">Archivo de configuración MFTrace</span><span class="sxs-lookup"><span data-stu-id="4c7e7-108">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)

## <a name="requirements"></a><span data-ttu-id="4c7e7-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c7e7-109">Requirements</span></span>



| <span data-ttu-id="4c7e7-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c7e7-110">Requirement</span></span> | <span data-ttu-id="4c7e7-111">Value</span><span class="sxs-lookup"><span data-stu-id="4c7e7-111">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c7e7-112">Versión mínima del SDK</span><span class="sxs-lookup"><span data-stu-id="4c7e7-112">Minimum SDK version</span></span>      | <span data-ttu-id="4c7e7-113">Kit de desarrollo de software (SDK) de Microsoft Windows para Windows 7 y .NET Framework 4,0</span><span class="sxs-lookup"><span data-stu-id="4c7e7-113">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span> |
| <span data-ttu-id="4c7e7-114">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="4c7e7-114">Minimum operating system</span></span> | <span data-ttu-id="4c7e7-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c7e7-115">Windows Vista</span></span>                                                                         |



 

<span data-ttu-id="4c7e7-116">MFTrace requiere los siguientes archivos dll, que también se proporcionan en el SDK.</span><span class="sxs-lookup"><span data-stu-id="4c7e7-116">MFTrace requires the following DLLs, which are also provided in the SDK.</span></span>

-   <span data-ttu-id="4c7e7-117">detoured.dll</span><span class="sxs-lookup"><span data-stu-id="4c7e7-117">detoured.dll</span></span>
-   <span data-ttu-id="4c7e7-118">mfdetours.dll</span><span class="sxs-lookup"><span data-stu-id="4c7e7-118">mfdetours.dll</span></span>

<span data-ttu-id="4c7e7-119">El SDK proporciona versiones de 32 bits y de 64 bits de MFTrace.</span><span class="sxs-lookup"><span data-stu-id="4c7e7-119">The SDK provides both 32-bit and 64-bit versions of MFTrace.</span></span> <span data-ttu-id="4c7e7-120">MFTrace no admite WOW64; para realizar el seguimiento de un proceso de 32 bits que se ejecuta en Windows de 64 bits, use la versión de 32 bits de MFTrace.</span><span class="sxs-lookup"><span data-stu-id="4c7e7-120">MFTrace does not support WOW64; to trace a 32-bit process running on 64-bit Windows, use the 32-bit version of MFTrace.</span></span>

<span data-ttu-id="4c7e7-121">SDK-root en sistemas de 32 bits: \Archivos de Programa\windows Kits\10 SDK-root on 64 bits System: \Archivos de programa (x86) \Windows Kits\10 encontrará mftrace en <SDK-root> \Bin \<sdk-version> \<architecture>\mftrace.exe</span><span class="sxs-lookup"><span data-stu-id="4c7e7-121">sdk-root on 32 bit systems: \Program Files\Windows Kits\10 sdk-root on 64 bit system: \Program Files (x86)\Windows Kits\10 You will find mftrace at <sdk-root>\bin\<sdk-version>\<architecture>\mftrace.exe</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c7e7-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4c7e7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c7e7-123">Herramientas de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4c7e7-123">Media Foundation Tools</span></span>](media-foundation-tools.md)
</dt> </dl>

 

 



