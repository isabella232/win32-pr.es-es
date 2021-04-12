---
description: Clasificaciones de mapas de bits
ms.assetid: 669ffaef-55c5-4cbc-b23a-de3d66bd6ab2
title: Clasificaciones de mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9632b2617eda6fc94ec4836f0e0aa4cc927af113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276026"
---
# <a name="bitmap-classifications"></a><span data-ttu-id="eea6d-103">Clasificaciones de mapas de bits</span><span class="sxs-lookup"><span data-stu-id="eea6d-103">Bitmap Classifications</span></span>

<span data-ttu-id="eea6d-104">Hay dos clases de mapas de bits:</span><span class="sxs-lookup"><span data-stu-id="eea6d-104">There are two classes of bitmaps:</span></span>

-   <span data-ttu-id="eea6d-105">[Mapas de bits independientes del dispositivo](device-independent-bitmaps.md) (DIB).</span><span class="sxs-lookup"><span data-stu-id="eea6d-105">[Device-independent bitmaps](device-independent-bitmaps.md) (DIB).</span></span> <span data-ttu-id="eea6d-106">El formato de archivo DIB se diseñó para asegurarse de que los gráficos de mapa Dete creados mediante una aplicación se pueden cargar y mostrar en otra aplicación, conservando el mismo aspecto que el original.</span><span class="sxs-lookup"><span data-stu-id="eea6d-106">The DIB file format was designed to ensure that bitmapped graphics created using one application can be loaded and displayed in another application, retaining the same appearance as the original.</span></span>

-   <span data-ttu-id="eea6d-107">Los [mapas de bits dependientes del dispositivo](device-dependent-bitmaps.md) (DDB), también conocidos como mapas de bits GDI, eran los únicos mapas de bits disponibles en las primeras versiones de Microsoft Windows de 16 bits (antes de la versión 3,0).</span><span class="sxs-lookup"><span data-stu-id="eea6d-107">[Device-dependent bitmaps](device-dependent-bitmaps.md) (DDB), also known as GDI bitmaps, were the only bitmaps available in early versions of 16-bit Microsoft Windows (prior to version 3.0).</span></span> <span data-ttu-id="eea6d-108">Sin embargo, a medida que la tecnología de visualización se ha mejorado y, a medida que aumenta el número de dispositivos de pantalla disponibles, se muestran algunos problemas inherentes que solo se pueden resolver mediante Dib.</span><span class="sxs-lookup"><span data-stu-id="eea6d-108">However, as display technology improved and as the variety of available display devices increased, certain inherent problems surfaced which could only be solved using DIBs.</span></span> <span data-ttu-id="eea6d-109">Por ejemplo, no había ningún método para almacenar (o recuperar) la resolución del tipo de presentación en el que se creó un mapa de bits, por lo que una aplicación de dibujo no podía determinar rápidamente si un mapa de bits era adecuado para el tipo de dispositivo de pantalla de vídeo en el que se ejecutaba la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eea6d-109">For example, there was no method of storing (or retrieving) the resolution of the display type on which a bitmap was created, so a drawing application could not quickly determine whether a bitmap was suitable for the type of video display device on which the application was running.</span></span>

    <span data-ttu-id="eea6d-110">A pesar de estos problemas, los DDBs (también conocidos como mapas de bits compatibles) siguen siendo útiles para mejorar el rendimiento de la GDI y para otras situaciones.</span><span class="sxs-lookup"><span data-stu-id="eea6d-110">Despite these problems, DDBs (also known as compatible bitmaps) are still useful for better GDI performance and for other situations.</span></span>

 

 



