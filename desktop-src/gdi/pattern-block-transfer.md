---
description: El nombre de la función PatBlt (una abreviatura para la transferencia de bloques de patrón) implica que esta función simplemente replica el pincel (o patrón) hasta que rellena un rectángulo especificado.
ms.assetid: 601e1e79-a328-4e63-958a-ca26129e03f8
title: Transferencia de bloque de patrón
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54424348c28b83d1d0d1075072e80b18049546ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997333"
---
# <a name="pattern-block-transfer"></a><span data-ttu-id="09e10-103">Transferencia de bloque de patrón</span><span class="sxs-lookup"><span data-stu-id="09e10-103">Pattern Block Transfer</span></span>

<span data-ttu-id="09e10-104">El nombre de la función [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) (una abreviatura para la transferencia de bloques de patrón) implica que esta función simplemente replica el pincel (o patrón) hasta que rellena un rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="09e10-104">The name of the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function (an abbreviation for pattern block transfer) implies that this function simply replicates the brush (or pattern) until it fills a specified rectangle.</span></span> <span data-ttu-id="09e10-105">Sin embargo, la función es realmente mucho más eficaz.</span><span class="sxs-lookup"><span data-stu-id="09e10-105">However, the function is actually much more powerful.</span></span> <span data-ttu-id="09e10-106">Antes de replicar el pincel, combina los datos de color del patrón con los datos de color de los píxeles existentes en la pantalla de vídeo mediante una operación de trama (ROP).</span><span class="sxs-lookup"><span data-stu-id="09e10-106">Before replicating the brush, it combines the color data for the pattern with the color data for the existing pixels on the video display by using a raster operation (ROP).</span></span> <span data-ttu-id="09e10-107">Un ROP es una operación bit a bit que se aplica a los bits de los datos de color del pincel replicado y los bits de los datos de color del rectángulo de destino en el dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="09e10-107">An ROP is a bitwise operation that is applied to the bits of color data for the replicated brush and the bits of color data for the target rectangle on the display device.</span></span> <span data-ttu-id="09e10-108">Hay 256 ROPs; sin embargo, la función **PatBlt** reconoce solo los que requieren un patrón y un destino (no los que requieren un origen).</span><span class="sxs-lookup"><span data-stu-id="09e10-108">There are 256 ROPs; however, the **PatBlt** function recognizes only those that require a pattern and a destination (not those that require a source).</span></span> <span data-ttu-id="09e10-109">En la tabla siguiente se identifica el ROPs más común.</span><span class="sxs-lookup"><span data-stu-id="09e10-109">The following table identifies the most common ROPs.</span></span>



| <span data-ttu-id="09e10-110">ROP</span><span class="sxs-lookup"><span data-stu-id="09e10-110">ROP</span></span>       | <span data-ttu-id="09e10-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="09e10-111">Description</span></span>                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="09e10-112">PATCOPY</span><span class="sxs-lookup"><span data-stu-id="09e10-112">PATCOPY</span></span>   | <span data-ttu-id="09e10-113">Copia el patrón en el mapa de bits de destino.</span><span class="sxs-lookup"><span data-stu-id="09e10-113">Copies the pattern to the destination bitmap.</span></span>                                       |
| <span data-ttu-id="09e10-114">PATINVERT</span><span class="sxs-lookup"><span data-stu-id="09e10-114">PATINVERT</span></span> | <span data-ttu-id="09e10-115">Combina el mapa de bits de destino con el patrón mediante el operador booleano XOR.</span><span class="sxs-lookup"><span data-stu-id="09e10-115">Combines the destination bitmap with the pattern by using the Boolean XOR operator.</span></span> |
| <span data-ttu-id="09e10-116">DSTINVERT</span><span class="sxs-lookup"><span data-stu-id="09e10-116">DSTINVERT</span></span> | <span data-ttu-id="09e10-117">Invierte el mapa de bits de destino.</span><span class="sxs-lookup"><span data-stu-id="09e10-117">Inverts the destination bitmap.</span></span>                                                     |
| <span data-ttu-id="09e10-118">De color negro</span><span class="sxs-lookup"><span data-stu-id="09e10-118">BLACKNESS</span></span> | <span data-ttu-id="09e10-119">Convierte todos los resultados en ceros binarios.</span><span class="sxs-lookup"><span data-stu-id="09e10-119">Turns all output to binary zeros.</span></span>                                                   |
| <span data-ttu-id="09e10-120">BLANCO</span><span class="sxs-lookup"><span data-stu-id="09e10-120">WHITENESS</span></span> | <span data-ttu-id="09e10-121">Convierte todos los resultados en binarios.</span><span class="sxs-lookup"><span data-stu-id="09e10-121">Turns all output to binary ones.</span></span>                                                    |



 

<span data-ttu-id="09e10-122">Para obtener más información, vea [códigos de operación de trama](raster-operation-codes.md).</span><span class="sxs-lookup"><span data-stu-id="09e10-122">For more information, see [Raster Operation Codes](raster-operation-codes.md).</span></span>

 

 



