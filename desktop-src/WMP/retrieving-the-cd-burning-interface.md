---
title: Recuperación de la interfaz de grabación de CD
description: Recuperación de la interfaz de grabación de CD
ms.assetid: d52f7b27-a327-4656-8dc2-0b075264d295
keywords:
- Windows Media Player, grabación de CD
- Modelo de objetos de Windows Media Player, grabación de CD
- modelo de objetos, grabación de CD
- Control ActiveX de Windows Media Player, grabación de CD
- Control ActiveX, grabación de CD
- Control ActiveX móvil de Windows Media Player, grabación de CD
- Windows Media Player Mobile, grabación de CD
- Grabación de CD, recuperación de la interfaz IWMPCdromCollection
- grabación de CDs, recuperación de la interfaz IWMPCdromCollection
- Interfaz IWMPCdromCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63763f9dd99bbaf88ae099edb53ba072cd1a25e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104077433"
---
# <a name="retrieving-the-cd-burning-interface"></a><span data-ttu-id="cb13c-113">Recuperación de la interfaz de grabación de CD</span><span class="sxs-lookup"><span data-stu-id="cb13c-113">Retrieving the CD Burning Interface</span></span>

<span data-ttu-id="cb13c-114">Para enumerar las unidades de CD en el equipo del usuario, use la interfaz **IWMPCdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="cb13c-114">To enumerate the CD drives on the user's computer, use the **IWMPCdromCollection** interface.</span></span> <span data-ttu-id="cb13c-115">Para recuperar un puntero a esta interfaz, llame a [IWMPCore:: get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span><span class="sxs-lookup"><span data-stu-id="cb13c-115">You retrieve a pointer to this interface by calling [IWMPCore::get\_cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span></span>

<span data-ttu-id="cb13c-116">Mediante el uso de los métodos **Get \_ Count** y **Item** , puede recorrer en iteración la colección para recuperar un puntero de la interfaz [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) para cada unidad de CD del equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="cb13c-116">By using the **get\_count** and **item** methods, you can iterate the collection to retrieve an [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) interface pointer for each CD drive on the user's computer.</span></span>

<span data-ttu-id="cb13c-117">La interfaz **IWMPCdrom** representa una unidad de CD individual.</span><span class="sxs-lookup"><span data-stu-id="cb13c-117">The **IWMPCdrom** interface represents an individual CD drive.</span></span> <span data-ttu-id="cb13c-118">Antes de empezar a grabar un CD, primero debe llamar a **QueryInterface** a través de un puntero **IWMPCdrom** para recuperar un puntero a la interfaz [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) .</span><span class="sxs-lookup"><span data-stu-id="cb13c-118">Before you begin burning a CD, you must first call **QueryInterface** through an **IWMPCdrom** pointer to retrieve a pointer to the [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface.</span></span>

<span data-ttu-id="cb13c-119">En el ejemplo de código siguiente se muestra cómo recuperar una interfaz para grabar un CD en una unidad específica:</span><span class="sxs-lookup"><span data-stu-id="cb13c-119">The following code example demonstrates how to retrieve an interface for burning a CD to a specific drive:</span></span>


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

    // Get the number of CDROM drives.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromCollection->get_count(&lDriveCount);
    }

    return hr;
}

// lIndex refers to the index of the current drive,
// which must be less than the value retrieved by
// GetCdromDriveCount above.
HRESULT CMainDlg::GetCdromBurnInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromBurn interface.
        m_spCdromBurn.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromBurn);
    }

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="cb13c-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cb13c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb13c-121">**Grabación de un CD**</span><span class="sxs-lookup"><span data-stu-id="cb13c-121">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="cb13c-122">**Iniciar el proceso de grabación**</span><span class="sxs-lookup"><span data-stu-id="cb13c-122">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="cb13c-123">**Borrado de un CD regrabable**</span><span class="sxs-lookup"><span data-stu-id="cb13c-123">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="cb13c-124">**Recuperación de la unidad y el estado del disco**</span><span class="sxs-lookup"><span data-stu-id="cb13c-124">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="cb13c-125">**Recuperación del estado de la grabación**</span><span class="sxs-lookup"><span data-stu-id="cb13c-125">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> <dt>

[<span data-ttu-id="cb13c-126">**Interfaz IWMPCdromCollection**</span><span class="sxs-lookup"><span data-stu-id="cb13c-126">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




