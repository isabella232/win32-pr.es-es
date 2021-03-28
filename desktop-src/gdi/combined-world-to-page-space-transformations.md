---
description: Las cinco transformaciones de mundo a página se pueden combinar en una sola matriz de 3 por 3.
ms.assetid: d17ba826-8e8d-4121-8afd-0f256121b54c
title: Transformaciones de espacio de página universal combinadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b770ef614fe1538a528de640cacc5ad54b28c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985026"
---
# <a name="combined-world-to-page-space-transformations"></a><span data-ttu-id="81648-103">Transformaciones de espacio de página universal combinadas</span><span class="sxs-lookup"><span data-stu-id="81648-103">Combined World-to-Page Space Transformations</span></span>

<span data-ttu-id="81648-104">Las cinco transformaciones de mundo a página se pueden combinar en una sola matriz de 3 por 3.</span><span class="sxs-lookup"><span data-stu-id="81648-104">The five world-to-page transformations can be combined into a single 3-by-3 matrix.</span></span> <span data-ttu-id="81648-105">La función [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) se puede usar para combinar dos transformaciones de espacio mundial en la página.</span><span class="sxs-lookup"><span data-stu-id="81648-105">The [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) function can be used to combine two world-space to page-space transformations.</span></span> <span data-ttu-id="81648-106">Las transformaciones combinadas se pueden usar para modificar la salida asociada a un contexto de dispositivo determinado (DC) mediante una llamada a la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) y proporcionando los elementos para esta matriz.</span><span class="sxs-lookup"><span data-stu-id="81648-106">The combined transformations can be used to alter output associated with a particular device context (DC) by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function and supplying the elements for this matrix.</span></span> <span data-ttu-id="81648-107">Cuando una aplicación llama a **SetWorldTransform**, almacena los elementos de la matriz de 3 por 3 en una estructura [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) .</span><span class="sxs-lookup"><span data-stu-id="81648-107">When an application calls **SetWorldTransform**, it stores the elements of the 3-by-3 matrix in an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span> <span data-ttu-id="81648-108">Los miembros de esta estructura se corresponden con las dos primeras columnas de una matriz de 3 por 3; la última columna de la matriz no es necesaria porque sus valores son constantes.</span><span class="sxs-lookup"><span data-stu-id="81648-108">The members of this structure correspond to the first two columns of a 3-by-3 matrix; the last column of the matrix is not required because its values are constant.</span></span>

<span data-ttu-id="81648-109">Los elementos de la matriz de transformación universal actual se pueden reactivar llamando a la función [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) y proporcionando un puntero a una estructura [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) .</span><span class="sxs-lookup"><span data-stu-id="81648-109">The elements of the current world transformation matrix can be revived by calling the [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) function and supplying a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span>

 

 



