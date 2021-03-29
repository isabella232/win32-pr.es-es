---
title: Aspectos básicos del compresor y el descompresor
description: Aspectos básicos del compresor y el descompresor
ms.assetid: 49a958c1-1798-4c6c-913c-5bf5869f926b
keywords:
- Administrador de compresión de vídeo (VCM), abrir compresores
- VCM (Administrador de compresión de vídeo), abrir compresores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b51e0221c495d5e2d0782f4e56e0778c0d2462
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903428"
---
# <a name="compressor-and-decompressor-basics"></a><span data-ttu-id="bc1a4-105">Aspectos básicos del compresor y el descompresor</span><span class="sxs-lookup"><span data-stu-id="bc1a4-105">Compressor and Decompressor Basics</span></span>

<span data-ttu-id="bc1a4-106">Para abrir y buscar un compresor, puede usar las funciones [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) y [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) .</span><span class="sxs-lookup"><span data-stu-id="bc1a4-106">To open and locate a compressor, you can use the [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) and [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) functions.</span></span> <span data-ttu-id="bc1a4-107">Puede usar **ICLocate** para buscar un compresor de un tipo específico y obtener un identificador para usarlo en otras funciones VCM.</span><span class="sxs-lookup"><span data-stu-id="bc1a4-107">You can use **ICLocate** to find a compressor of a specific type and to obtain a handle of it for use in other VCM functions.</span></span> <span data-ttu-id="bc1a4-108">Para abrir un compresor, puede usar **ICOpen**.</span><span class="sxs-lookup"><span data-stu-id="bc1a4-108">To open a compressor, you can use **ICOpen**.</span></span> <span data-ttu-id="bc1a4-109">La aplicación usa el identificador devuelto por esta función para identificar el compresor abierto cuando utiliza otras funciones VCM.</span><span class="sxs-lookup"><span data-stu-id="bc1a4-109">Your application uses the handle returned by this function to identify the opened compressor when it uses other VCM functions.</span></span>

<span data-ttu-id="bc1a4-110">Para abrir y buscar un descompresor, las aplicaciones pueden usar las macros [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) y [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) .</span><span class="sxs-lookup"><span data-stu-id="bc1a4-110">To open and locate a decompressor, applications can use the [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) and [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) macros.</span></span> <span data-ttu-id="bc1a4-111">Estas macros usan **ICLocate** para la operación.</span><span class="sxs-lookup"><span data-stu-id="bc1a4-111">These macros use **ICLocate** for operation.</span></span>

<span data-ttu-id="bc1a4-112">Cuando la aplicación ha terminado de usar un compresor o descompresor, debe cerrarla para liberar los recursos utilizados para la compresión o la descompresión.</span><span class="sxs-lookup"><span data-stu-id="bc1a4-112">When your application has finished using a compressor or decompressor, it must close it to free any resources used for compression or decompression.</span></span> <span data-ttu-id="bc1a4-113">La aplicación puede usar la función [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) para cerrar el compresor o descompresor.</span><span class="sxs-lookup"><span data-stu-id="bc1a4-113">Your application can use the [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) function to close the compressor or decompressor.</span></span>

<span data-ttu-id="bc1a4-114">Además, la aplicación puede enumerar los compresores o descompresores en un sistema mediante la función [**ICInfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) .</span><span class="sxs-lookup"><span data-stu-id="bc1a4-114">Also, your application can enumerate the compressors or decompressors on a system by using the [**ICInfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) function.</span></span>

> [!Note]  
> <span data-ttu-id="bc1a4-115">El encabezado de secuencia de un archivo AVI contiene información sobre el tipo de flujo y el controlador específico para ese flujo.</span><span class="sxs-lookup"><span data-stu-id="bc1a4-115">The stream header in an AVI file contains information about the stream type and the specific handler for that stream.</span></span> <span data-ttu-id="bc1a4-116">Dentro del encabezado de flujo, los miembros **fccType** y **fccHandler** identifican el tipo de flujo y el controlador de secuencia especificado para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="bc1a4-116">Within the stream header, the **fccType** and **fccHandler** members identify the stream type and the stream handler specified for the stream.</span></span>

 

 

 




