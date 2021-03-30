---
title: Recuperación de la unidad y el estado del disco
description: Recuperación de la unidad y el estado del disco
ms.assetid: 5e3e6107-d2bc-450c-a86e-5d3ef7b3092a
keywords:
- Windows Media Player, grabación de CD
- Modelo de objetos de Windows Media Player, grabación de CD
- modelo de objetos, grabación de CD
- Control ActiveX de Windows Media Player, grabación de CD
- Control ActiveX, grabación de CD
- Control ActiveX móvil de Windows Media Player, grabación de CD
- Windows Media Player Mobile, grabación de CD
- Grabación de CD, recuperación de la unidad y el estado del disco
- grabar CDs, recuperar el estado de unidades y discos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eab66581c336f642fd53b22f81949847d0a1c89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103904413"
---
# <a name="retrieving-the-drive-and-disc-status"></a><span data-ttu-id="7321c-112">Recuperación de la unidad y el estado del disco</span><span class="sxs-lookup"><span data-stu-id="7321c-112">Retrieving the Drive and Disc Status</span></span>

<span data-ttu-id="7321c-113">Antes de iniciar una operación de grabación de CD, debe asegurarse de que la unidad de CD-ROM seleccionada sea compatible con la operación que desea realizar.</span><span class="sxs-lookup"><span data-stu-id="7321c-113">Before starting a CD burning operation, you must ensure that the selected CD-ROM drive supports the operation you want to perform.</span></span> <span data-ttu-id="7321c-114">Por ejemplo, debe comprobar que se puede borrar un CD antes de llamar a [IWMPCdromBurn:: Erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span><span class="sxs-lookup"><span data-stu-id="7321c-114">For instance, you must check that a CD is capable of being erased before calling [IWMPCdromBurn::erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span></span> <span data-ttu-id="7321c-115">En el código siguiente se muestra un ejemplo del uso de [IWMPCdromBurn:: isavailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) para determinar si se admite una operación:</span><span class="sxs-lookup"><span data-stu-id="7321c-115">The following code shows an example of using [IWMPCdromBurn::isAvailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) to determine whether an operation is supported:</span></span>


```C++
VARIANT_BOOL vbResult;
    
// Check whether this drive can burn CDs.
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("Burn");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->isAvailable(bstrItem, &vbResult);
}
if (SUCCEEDED(hr))
{
    if (VARIANT_TRUE == vbResult)
    {
        // The current drive can burn CDs.
    }
}

```



## <a name="related-topics"></a><span data-ttu-id="7321c-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7321c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7321c-117">**Grabación de un CD**</span><span class="sxs-lookup"><span data-stu-id="7321c-117">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="7321c-118">**Recuperación de la interfaz de grabación de CD**</span><span class="sxs-lookup"><span data-stu-id="7321c-118">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="7321c-119">**Iniciar el proceso de grabación**</span><span class="sxs-lookup"><span data-stu-id="7321c-119">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="7321c-120">**Borrado de un CD regrabable**</span><span class="sxs-lookup"><span data-stu-id="7321c-120">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="7321c-121">**Recuperación del estado de la grabación**</span><span class="sxs-lookup"><span data-stu-id="7321c-121">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




