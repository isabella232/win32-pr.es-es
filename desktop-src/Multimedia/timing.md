---
title: Temporización (Windows multimedia)
description: Control de tiempo
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- DrawDib, temporización
- DrawDibTime función)
- DrawDib, depuración
- depurar DrawDib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adddd43ff5067d08334a40f2e52e79109c8a8bb7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488753"
---
# <a name="timing-windows-multimedia"></a><span data-ttu-id="dbc44-107">Temporización (Windows multimedia)</span><span class="sxs-lookup"><span data-stu-id="dbc44-107">Timing (Windows Multimedia)</span></span>

<span data-ttu-id="dbc44-108">Como parte de la depuración de una aplicación, puede obtener información sobre la cantidad de tiempo necesario para completar las operaciones repetitivas de DrawDib.</span><span class="sxs-lookup"><span data-stu-id="dbc44-108">As part of debugging an application, you can obtain information about the amount of time required to complete repetitive DrawDib operations.</span></span> <span data-ttu-id="dbc44-109">La función [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) devuelve información de tiempo para las siguientes operaciones:</span><span class="sxs-lookup"><span data-stu-id="dbc44-109">The [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) function returns timing information for the following operations:</span></span>

-   <span data-ttu-id="dbc44-110">Dibujo de un mapa de bits</span><span class="sxs-lookup"><span data-stu-id="dbc44-110">Drawing a bitmap</span></span>
-   <span data-ttu-id="dbc44-111">Descomprimir un mapa de bits</span><span class="sxs-lookup"><span data-stu-id="dbc44-111">Decompressing a bitmap</span></span>
-   <span data-ttu-id="dbc44-112">Tramar un mapa de bits</span><span class="sxs-lookup"><span data-stu-id="dbc44-112">Dithering a bitmap</span></span>
-   <span data-ttu-id="dbc44-113">Ajustar un mapa de bits</span><span class="sxs-lookup"><span data-stu-id="dbc44-113">Stretching a bitmap</span></span>
-   <span data-ttu-id="dbc44-114">Transferir un mapa de bits mediante la función [**bitblt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt)</span><span class="sxs-lookup"><span data-stu-id="dbc44-114">Transferring a bitmap by using the [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) function</span></span>
-   <span data-ttu-id="dbc44-115">Transferir un mapa de bits mediante la función [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)</span><span class="sxs-lookup"><span data-stu-id="dbc44-115">Transferring a bitmap by using the [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) function</span></span>

<span data-ttu-id="dbc44-116">Después de recuperar un conjunto de valores, [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) restablece el recuento y el valor de cada operación.</span><span class="sxs-lookup"><span data-stu-id="dbc44-116">After retrieving a set of values, [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) resets the count and value for each operation.</span></span>

<span data-ttu-id="dbc44-117">La función [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) solo está disponible en la versión de depuración de las funciones DrawDib.</span><span class="sxs-lookup"><span data-stu-id="dbc44-117">The [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) function is available only in the debug version of the DrawDib functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbc44-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dbc44-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbc44-119">Representación de imágenes</span><span class="sxs-lookup"><span data-stu-id="dbc44-119">Image Rendering</span></span>](image-rendering.md)
</dt> </dl>

 

 
