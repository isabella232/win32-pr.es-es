---
description: Si se establece este bit, se crean las imágenes en el cuadro de diálogo con la paleta personalizada (una por cada cuadro de diálogo recibido del primer control creado). Si no se establece el bit, las imágenes se representan utilizando una paleta predeterminada.
ms.assetid: 9cfc7fd9-27a3-4208-b42c-48369890a74b
title: Bit de estilo del cuadro de diálogo UseCustomPalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507ed1c900c564e3e791f4d0bbc5f8658798fdb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653049"
---
# <a name="usecustompalette-dialog-style-bit"></a><span data-ttu-id="6991d-104">Bit de estilo del cuadro de diálogo UseCustomPalette</span><span class="sxs-lookup"><span data-stu-id="6991d-104">UseCustomPalette Dialog Style Bit</span></span>

<span data-ttu-id="6991d-105">Si se establece este bit, se crean las imágenes en el cuadro de diálogo con la paleta personalizada (una por cada cuadro de diálogo recibido del primer control creado).</span><span class="sxs-lookup"><span data-stu-id="6991d-105">If this bit is set, the pictures on the dialog box are created with the custom palette (one per dialog received from the first control created).</span></span> <span data-ttu-id="6991d-106">Si no se establece el bit, las imágenes se representan utilizando una paleta predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6991d-106">If the bit is not set, the pictures are rendered using a default palette.</span></span>

<span data-ttu-id="6991d-107">Normalmente, se establece este bit si el cuadro de diálogo contiene una imagen con una paleta especial o varias imágenes que comparten una paleta personalizada.</span><span class="sxs-lookup"><span data-stu-id="6991d-107">Typically one would set this bit if the dialog contains a picture with a special palette, or several pictures sharing a custom palette.</span></span> <span data-ttu-id="6991d-108">No se debe establecer el bit si el cuadro de diálogo contiene varias imágenes con diferentes paletas.</span><span class="sxs-lookup"><span data-stu-id="6991d-108">The bit should not be set if the dialog contains several pictures with different palettes.</span></span> <span data-ttu-id="6991d-109">En este caso, es más probable que la paleta predeterminada proporcione un resultado satisfactorio para todas las imágenes.</span><span class="sxs-lookup"><span data-stu-id="6991d-109">In this case, the default palette is most likely to give a satisfactory result for all pictures.</span></span>

## <a name="value"></a><span data-ttu-id="6991d-110">Value</span><span class="sxs-lookup"><span data-stu-id="6991d-110">Value</span></span>



| <span data-ttu-id="6991d-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="6991d-111">Decimal</span></span> | <span data-ttu-id="6991d-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="6991d-112">Hexadecimal</span></span> | <span data-ttu-id="6991d-113">Constante</span><span class="sxs-lookup"><span data-stu-id="6991d-113">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="6991d-114">64</span><span class="sxs-lookup"><span data-stu-id="6991d-114">64</span></span>      | <span data-ttu-id="6991d-115">0x00000040</span><span class="sxs-lookup"><span data-stu-id="6991d-115">0x00000040</span></span>  | <span data-ttu-id="6991d-116">**msidbDialogAttributesUseCustomPalette**</span><span class="sxs-lookup"><span data-stu-id="6991d-116">**msidbDialogAttributesUseCustomPalette**</span></span> |



 

 

 



