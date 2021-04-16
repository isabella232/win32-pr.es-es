---
title: Crear secuencias temporales
description: Crear secuencias temporales
ms.assetid: 8fe75ae1-0111-4b02-a00d-1ef2ca462452
keywords:
- AVIStreamCreate función)
- AVIStreamRelease función)
- AVIMakeCompressedStream función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209259f46e25275094dcd1eb5eeddd4f336ee906
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486759"
---
# <a name="creating-temporary-streams"></a><span data-ttu-id="b3e0a-106">Crear secuencias temporales</span><span class="sxs-lookup"><span data-stu-id="b3e0a-106">Creating Temporary Streams</span></span>

<span data-ttu-id="b3e0a-107">Las secuencias temporales pueden ser beneficiosas de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="b3e0a-107">Temporary streams can be beneficial in several ways.</span></span> <span data-ttu-id="b3e0a-108">Puede usar una secuencia temporal como flujo de trabajo, por ejemplo, al cambiar el formato de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b3e0a-108">You can use a temporary stream as a work stream, for example, when changing the stream format.</span></span> <span data-ttu-id="b3e0a-109">O bien, puede crear una secuencia temporal para almacenar partes de otros flujos que se han copiado.</span><span class="sxs-lookup"><span data-stu-id="b3e0a-109">Or you can create a temporary stream to hold portions of other streams that have been copied.</span></span>

<span data-ttu-id="b3e0a-110">Puede crear una secuencia en memoria que no está asociada a ningún archivo mediante la función [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) .</span><span class="sxs-lookup"><span data-stu-id="b3e0a-110">You can create a stream in memory that is not associated with any file by using the [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) function.</span></span> <span data-ttu-id="b3e0a-111">Esta función devuelve la dirección de la interfaz a la nueva secuencia en una ubicación especificada y la usan internamente otras funciones que crean secuencias temporales.</span><span class="sxs-lookup"><span data-stu-id="b3e0a-111">This function returns the address of the interface to the new stream in a specified location and is used internally by other functions that create temporary streams.</span></span>

<span data-ttu-id="b3e0a-112">Puede crear un flujo comprimido a partir de una secuencia sin comprimir mediante la función [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) .</span><span class="sxs-lookup"><span data-stu-id="b3e0a-112">You can create a compressed stream from an uncompressed stream by using the [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) function.</span></span> <span data-ttu-id="b3e0a-113">Identifique la secuencia que se va a comprimir, el método de compresión y las opciones de compresión, y el controlador del nuevo flujo.</span><span class="sxs-lookup"><span data-stu-id="b3e0a-113">You identify the stream to compress, the compression method and compression options, and the handler for the new stream.</span></span>

<span data-ttu-id="b3e0a-114">Cuando termine de usar una secuencia creada con **AVIStreamCreate** o **AVIMakeCompressedStream**, cierre la secuencia mediante la función [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) .</span><span class="sxs-lookup"><span data-stu-id="b3e0a-114">When you finish using a stream created with **AVIStreamCreate** or **AVIMakeCompressedStream**, close the stream by using the [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) function.</span></span> <span data-ttu-id="b3e0a-115">**AVIStreamRelease** libera los recursos utilizados por la secuencia temporal.</span><span class="sxs-lookup"><span data-stu-id="b3e0a-115">**AVIStreamRelease** frees the resources the temporary stream used.</span></span>

 

 




