---
title: Recuperación de la interfaz de copia desde CD
description: Recuperación de la interfaz de copia desde CD
ms.assetid: 760610eb-e356-4b50-b865-53557ba9b815
keywords:
- Windows Media Player, copia desde CD
- Modelo de objetos de Windows Media Player, copia desde CD
- modelo de objetos, copia desde CD
- Control ActiveX de Windows Media Player, copia desde CD
- Control ActiveX, copiar CD
- Control ActiveX móvil de Windows Media Player, copia desde CD
- Windows Media Player Mobile, copia desde CD
- Copia desde CD, interfaz de IWMPCdromRip
- copia desde CD, interfaz de IWMPCdromRip
- Interfaz IWMPCdromRip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903fa285404700e35363a94239c79706e7af0e34
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103904439"
---
# <a name="retrieving-the-ripping-interface"></a><span data-ttu-id="7c915-113">Recuperación de la interfaz de copia desde CD</span><span class="sxs-lookup"><span data-stu-id="7c915-113">Retrieving the Ripping Interface</span></span>

<span data-ttu-id="7c915-114">Para enumerar las unidades de CD en el equipo del usuario, use la interfaz **IWMPCdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="7c915-114">To enumerate the CD drives on the user's computer, use the **IWMPCdromCollection** interface.</span></span> <span data-ttu-id="7c915-115">Recupere un puntero a esta interfaz llamando a [IWMPCore:: get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span><span class="sxs-lookup"><span data-stu-id="7c915-115">Retrieve a pointer to this interface by calling [IWMPCore::get\_cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span></span>

<span data-ttu-id="7c915-116">Mediante el uso de los métodos [Get \_ Count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) y [Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) , puede recorrer en iteración la colección para recuperar una interfaz [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) para cada unidad de CD en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="7c915-116">By using the [get\_count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) and [item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) methods, you can iterate the collection to retrieve an [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) interface for each CD drive on the user's computer.</span></span>

<span data-ttu-id="7c915-117">La interfaz **IWMPCdrom** representa una unidad de CD individual.</span><span class="sxs-lookup"><span data-stu-id="7c915-117">The **IWMPCdrom** interface represents an individual CD drive.</span></span> <span data-ttu-id="7c915-118">Antes de empezar a copiar un CD, primero debe llamar a **QueryInterface** a través de un puntero **IWMPCdrom** para recuperar la interfaz [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) .</span><span class="sxs-lookup"><span data-stu-id="7c915-118">Before you begin ripping a CD, you must first call **QueryInterface** through an **IWMPCdrom** pointer to retrieve the [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) interface.</span></span>

<span data-ttu-id="7c915-119">En el ejemplo de código siguiente se muestra cómo recuperar una interfaz para copiar desde CD desde una unidad específica:</span><span class="sxs-lookup"><span data-stu-id="7c915-119">The following code example demonstrates how to retrieve an interface for ripping a CD from a specific drive:</span></span>


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    HRESULT hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

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
HRESULT CMainDlg::GetCdromRipInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromRip interface.
        m_spCdromRip.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromRip);
    }

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="7c915-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7c915-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c915-121">**Copia desde CD**</span><span class="sxs-lookup"><span data-stu-id="7c915-121">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="7c915-122">**Inicio del proceso RIP**</span><span class="sxs-lookup"><span data-stu-id="7c915-122">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="7c915-123">**Recuperación del estado de RIP**</span><span class="sxs-lookup"><span data-stu-id="7c915-123">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> <dt>

[<span data-ttu-id="7c915-124">**Seleccionar elementos para copiar desde CD**</span><span class="sxs-lookup"><span data-stu-id="7c915-124">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> <dt>

[<span data-ttu-id="7c915-125">**Interfaz IWMPCdromCollection**</span><span class="sxs-lookup"><span data-stu-id="7c915-125">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




