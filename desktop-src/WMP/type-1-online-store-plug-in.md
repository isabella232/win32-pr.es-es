---
title: Escriba 1 complemento de tienda en línea
description: Escriba 1 complemento de tienda en línea
ms.assetid: 3aa74282-522b-4240-8d72-73bd3015abeb
keywords:
- Windows Media Player tiendas en línea, Complementos
- tiendas en línea, Complementos
- tipo 1 tiendas en línea, Complementos
- Windows Media Player tiendas en línea, interfaz IWMPContentPartner
- tiendas en línea, interfaz IWMPContentPartner
- tipo 1 tiendas en línea, interfaz IWMPContentPartner
- complementos, Windows Media Player tiendas en línea
- complementos, tiendas en línea
- complementos, escriba 1 tiendas en línea
- complementos, interfaz IWMPContentPartner
- Complementos de Windows Media Player, escriba 1 tiendas en línea
- Complementos de Windows Media Player, tiendas en línea
- Complementos de Windows Media Player, Windows Media Player tiendas en línea
- Complementos de Media Player de Windows, interfaz IWMPContentPartner
- IWMPContentPartner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe42095d08262520734603a5418ac6831ce6685
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104077452"
---
# <a name="type-1-online-store-plug-in"></a><span data-ttu-id="b751f-118">Escriba 1 complemento de tienda en línea</span><span class="sxs-lookup"><span data-stu-id="b751f-118">Type 1 Online Store Plug-in</span></span>

<span data-ttu-id="b751f-119">Para aprovechar las características de integración de bibliotecas, escriba 1 los proveedores de tiendas en línea deben crear un complemento que implemente la interfaz [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) .</span><span class="sxs-lookup"><span data-stu-id="b751f-119">To take advantage of library integration features, type 1 online store providers must create a plug-in that implements the [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="b751f-120">Esta interfaz proporciona los métodos que Windows Media Player llama para notificar a la tienda en línea sobre las actividades que se realizan en el reproductor y para recuperar información específica sobre el contenido de la tienda en línea, el catálogo o el propio almacén.</span><span class="sxs-lookup"><span data-stu-id="b751f-120">This interface provides the methods that Windows Media Player calls to notify the online store about activities taking place in the Player and to retrieve specific information about online store content, the catalog, or the store itself.</span></span>

<span data-ttu-id="b751f-121">Una vez que Windows Media Player crea instancias del complemento, el reproductor llama a [IWMPContentPartner:: SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback)y proporciona un puntero a la interfaz **IWMPContentPartnerCallback** .</span><span class="sxs-lookup"><span data-stu-id="b751f-121">After Windows Media Player instantiates the plug-in, the Player calls [IWMPContentPartner::SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback), and provides a pointer to the **IWMPContentPartnerCallback** interface.</span></span> <span data-ttu-id="b751f-122">Esta interfaz proporciona a la tienda en línea una forma de realizar llamadas en Media Player de Windows para proporcionar información de estado o para iniciar procesos específicos, como la descarga de una pista de música.</span><span class="sxs-lookup"><span data-stu-id="b751f-122">This interface gives the online store a way to make calls into Windows Media Player to provide status information or to initiate specific processes, such as downloading a music track.</span></span>

<span data-ttu-id="b751f-123">Windows Media Player y el complemento se ejecutan en procesos independientes.</span><span class="sxs-lookup"><span data-stu-id="b751f-123">Windows Media Player and the plug-in run in separate processes.</span></span> <span data-ttu-id="b751f-124">El complemento es un servidor en proceso que se ejecuta en el suplente de DLL predeterminado, dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="b751f-124">The plug-in is an in-process server that runs in the default DLL surrogate, dllhost.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b751f-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b751f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b751f-126">**Acerca de las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="b751f-126">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="b751f-127">**Interfaz IWMPContentPartner**</span><span class="sxs-lookup"><span data-stu-id="b751f-127">**IWMPContentPartner Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> <dt>

[<span data-ttu-id="b751f-128">**Interfaz IWMPContentPartnerCallback**</span><span class="sxs-lookup"><span data-stu-id="b751f-128">**IWMPContentPartnerCallback Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)
</dt> </dl>

 

 




