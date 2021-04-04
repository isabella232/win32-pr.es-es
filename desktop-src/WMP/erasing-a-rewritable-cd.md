---
title: Borrado de un CD regrabable
description: Borrado de un CD regrabable
ms.assetid: 272fdd2b-c174-4bde-b05e-839d547532a6
keywords:
- Windows Media Player, grabación de CD
- Modelo de objetos de Windows Media Player, grabación de CD
- modelo de objetos, grabación de CD
- Control ActiveX de Windows Media Player, grabación de CD
- Control ActiveX, grabación de CD
- Control ActiveX móvil de Windows Media Player, grabación de CD
- Windows Media Player Mobile, grabación de CD
- Grabación de CD, borrar CDs regrabables
- grabar CDs, borrar CDs regrabables
- borrado de CDs regrabables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7025b7cd70c86c0b832aa792e50a8a2c64e7f45
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077316"
---
# <a name="erasing-a-rewritable-cd"></a><span data-ttu-id="f00c5-113">Borrado de un CD regrabable</span><span class="sxs-lookup"><span data-stu-id="f00c5-113">Erasing a Rewritable CD</span></span>

<span data-ttu-id="f00c5-114">La interfaz [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) proporciona un método para borrar los discos CD-RW.</span><span class="sxs-lookup"><span data-stu-id="f00c5-114">The [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface provides a method for erasing CD-RW discs.</span></span> <span data-ttu-id="f00c5-115">Antes de borrar un CD, primero debe asegurarse de que se admite la operación.</span><span class="sxs-lookup"><span data-stu-id="f00c5-115">Before erasing a CD, you must first ensure that the operation is supported.</span></span> <span data-ttu-id="f00c5-116">Para obtener más información, consulte [recuperar el estado de la unidad y del disco](retrieving-the-drive-and-disc-status.md).</span><span class="sxs-lookup"><span data-stu-id="f00c5-116">For more information, see [Retrieving the Drive and Disc Status](retrieving-the-drive-and-disc-status.md).</span></span>

<span data-ttu-id="f00c5-117">Para empezar a borrar el contenido de un CD regrabable, llame a [IWMPCdromBurn:: Erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span><span class="sxs-lookup"><span data-stu-id="f00c5-117">To begin erasing the contents of a rewritable CD, call [IWMPCdromBurn::erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span></span>


```C++

    HRESULT hr = m_spCdromBurn->erase();
    

```



## <a name="related-topics"></a><span data-ttu-id="f00c5-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f00c5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f00c5-119">**Grabación de un CD**</span><span class="sxs-lookup"><span data-stu-id="f00c5-119">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="f00c5-120">**Recuperación de la interfaz de grabación de CD**</span><span class="sxs-lookup"><span data-stu-id="f00c5-120">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="f00c5-121">**Iniciar el proceso de grabación**</span><span class="sxs-lookup"><span data-stu-id="f00c5-121">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="f00c5-122">**Recuperación de la unidad y el estado del disco**</span><span class="sxs-lookup"><span data-stu-id="f00c5-122">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="f00c5-123">**Recuperación del estado de la grabación**</span><span class="sxs-lookup"><span data-stu-id="f00c5-123">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




