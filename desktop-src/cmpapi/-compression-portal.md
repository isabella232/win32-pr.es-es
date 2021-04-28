---
description: API de compresión
ms.assetid: 3ef35cd0-3742-4fc2-9c06-e0485d3538f2
title: API de compresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e088b37bbe2ba652379a2d90e6e1e21f87a2e68
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087993"
---
# <a name="compression-api"></a><span data-ttu-id="caf16-103">API de compresión</span><span class="sxs-lookup"><span data-stu-id="caf16-103">Compression API</span></span>

## <a name="purpose"></a><span data-ttu-id="caf16-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="caf16-104">Purpose</span></span>

<span data-ttu-id="caf16-105">La API de compresión expone los algoritmos de compresión MSZIP, XPRESS, XPRESS HUFF y \_ LZMS de Windows.</span><span class="sxs-lookup"><span data-stu-id="caf16-105">The Compression API exposes the Windows MSZIP, XPRESS, XPRESS\_HUFF, and LZMS compression algorithms.</span></span> <span data-ttu-id="caf16-106">Esto permite a los desarrolladores de aplicaciones de Windows administrar versiones, servicios y ampliar los algoritmos de compresión expuestos.</span><span class="sxs-lookup"><span data-stu-id="caf16-106">This enables developers of Windows applications to manage versions, service, and extend the exposed compression algorithms.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="caf16-107">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="caf16-107">Developer audience</span></span>

<span data-ttu-id="caf16-108">Compression API está diseñada para su uso por parte de desarrolladores profesionales de C/C++ de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="caf16-108">The Compression API is designed for use by professional C/C++ developers of Windows applications.</span></span> <span data-ttu-id="caf16-109">La API de compresión expone los algoritmos de compresión sin pérdida usados por Windows a través de una interfaz pública y una API en modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="caf16-109">The Compression API exposes the lossless compression algorithms used by Windows though a public interface and user-mode API.</span></span> <span data-ttu-id="caf16-110">Compression API es el método recomendado para que los desarrolladores de Windows controle los algoritmos de compresión.</span><span class="sxs-lookup"><span data-stu-id="caf16-110">The Compression API is the recommended method for Windows developers to control the compression algorithms.</span></span> <span data-ttu-id="caf16-111">Esta característica es de 64 bits en Windows de 64 bits y de 32 bits en Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="caf16-111">This feature is 64-bit on 64-bit Windows and 32-bit on 32-bit Windows.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="caf16-112">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="caf16-112">Run-time requirements</span></span>

<span data-ttu-id="caf16-113">Compression API está disponible a partir de Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="caf16-113">The Compression API is available beginning with the Windows 8 or Windows Server 2012.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="caf16-114">En esta sección</span><span class="sxs-lookup"><span data-stu-id="caf16-114">In this section</span></span>

-   [<span data-ttu-id="caf16-115">Uso de compression API</span><span class="sxs-lookup"><span data-stu-id="caf16-115">Using the Compression API</span></span>](using-the-compression-api.md)
-   [<span data-ttu-id="caf16-116">Funciones de la API de compresión</span><span class="sxs-lookup"><span data-stu-id="caf16-116">Compression API Functions</span></span>](compression-api-functions.md)
-   [<span data-ttu-id="caf16-117">Estructuras de api de compresión</span><span class="sxs-lookup"><span data-stu-id="caf16-117">Compression API Structures</span></span>](compression-api-structures.md)
-   [<span data-ttu-id="caf16-118">Enumeraciones de API de compresión</span><span class="sxs-lookup"><span data-stu-id="caf16-118">Compression API Enumerations</span></span>](compression-api-enumerations.md)

 

 



