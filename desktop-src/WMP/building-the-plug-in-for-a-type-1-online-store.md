---
title: Compilar el complemento para una tienda en línea de tipo 1
description: Compilar el complemento para una tienda en línea de tipo 1
ms.assetid: 5d38a41f-9859-452b-953f-3449c2b0ce06
keywords:
- Windows Media Player tiendas en línea, Complementos
- tiendas en línea, Complementos
- tipo 1 tiendas en línea, Complementos
- Windows Media Player tiendas en línea, generar complementos
- tiendas en línea, crear complementos
- Escriba 1 almacenes en línea, compilando complementos
- Windows Media Player tiendas en línea, interfaz IWMPContentPartner
- tiendas en línea, interfaz IWMPContentPartner
- tipo 1 tiendas en línea, interfaz IWMPContentPartner
- complementos, Windows Media Player tiendas en línea
- complementos, tiendas en línea
- complementos, escriba 1 tiendas en línea
- complementos, interfaz IWMPContentPartner
- complementos, compilar
- Complementos de Windows Media Player, escriba 1 tiendas en línea
- Complementos de Windows Media Player, tiendas en línea
- Complementos de Windows Media Player, Windows Media Player tiendas en línea
- Complementos de Media Player de Windows, interfaz IWMPContentPartner
- Complementos de Windows Media Player, compilar
- IWMPContentPartner
- crear complementos, tipo 1 tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36272e3497eebc7b5362d793a0ee265d2c3166fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695560"
---
# <a name="building-the-plug-in-for-a-type-1-online-store"></a><span data-ttu-id="f8008-124">Compilar el complemento para una tienda en línea de tipo 1</span><span class="sxs-lookup"><span data-stu-id="f8008-124">Building the Plug-in for a Type 1 Online Store</span></span>

<span data-ttu-id="f8008-125">Una tienda en línea de tipo 1 debe proporcionar un complemento que implemente la interfaz [**IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) .</span><span class="sxs-lookup"><span data-stu-id="f8008-125">A type 1 online store must provide a plug-in that implements the [**IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="f8008-126">El complemento se ejecuta en un proceso independiente del Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="f8008-126">The plug-in runs in a separate process from Windows Media Player.</span></span>

<span data-ttu-id="f8008-127">Los pasos para crear un complemento que se ejecuta fuera de proceso son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f8008-127">The steps for creating a plug-in that runs out-of-process are as follows:</span></span>

1.  <span data-ttu-id="f8008-128">Escriba el complemento como si fuera un servidor COM en proceso.</span><span class="sxs-lookup"><span data-stu-id="f8008-128">Write your plug-in as if it were an in-process COM server.</span></span>
2.  <span data-ttu-id="f8008-129">Cree una entrada del registro **DllSurrogate** en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="f8008-129">Create a **DllSurrogate** registry entry on the user's computer.</span></span> <span data-ttu-id="f8008-130">La entrada **DllSurrogate** informa al tiempo de ejecución de com que el complemento debe crearse en una instancia del suplente de dll predeterminado, dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="f8008-130">The **DllSurrogate** entry informs the COM runtime that your plug-in should be created in an instance of the default DLL surrogate, dllhost.exe.</span></span>

<span data-ttu-id="f8008-131">Para obtener información detallada sobre cómo registrar el complemento, consulte [claves del registro y entradas para una tienda en línea de tipo 1](registry-keys-and-entries-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="f8008-131">For detailed information about registering your plug-in, see [Registry Keys and Entries for a Type 1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="f8008-132">No es necesario crear ningún código auxiliar o proxy para el complemento.</span><span class="sxs-lookup"><span data-stu-id="f8008-132">You do not need to create any proxy or stub code for your plug-in.</span></span> <span data-ttu-id="f8008-133">Toda la compatibilidad con la serialización la proporciona Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f8008-133">All of the marshaling support is provided by Windows Media Player.</span></span>

<span data-ttu-id="f8008-134">Puede usar el Asistente para complementos de tienda en línea para crear rápidamente un complemento que sirve como punto de partida.</span><span class="sxs-lookup"><span data-stu-id="f8008-134">You can use the online store plug-in wizard to quickly create a plug-in that serves as a starting point.</span></span> <span data-ttu-id="f8008-135">Para obtener más información, consulte [instalar el complemento de la tienda en línea](installing-the-online-store-plug-in-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="f8008-135">For more information, see [Installing the Online Store Plug-in Wizard](installing-the-online-store-plug-in-wizard.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8008-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f8008-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8008-137">**Guía de programación para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="f8008-137">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




