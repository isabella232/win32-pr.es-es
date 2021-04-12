---
title: Límites de carga
description: Para limitar el tamaño de las cargas, establezca la propiedad de extensión de IIS BITSMaximumUploadSize.
ms.assetid: 01ad2f32-18be-43a5-a07f-e6f28f7a471b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647aeefe82cf9c3ab035bc3e233c4157f471110b
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104487295"
---
# <a name="upload-limits"></a><span data-ttu-id="44d22-103">Límites de carga</span><span class="sxs-lookup"><span data-stu-id="44d22-103">Upload Limits</span></span>

<span data-ttu-id="44d22-104">Para limitar el tamaño de las cargas, establezca la propiedad de extensión de IIS [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="44d22-104">To limit the size of uploads, set the [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) IIS extension property.</span></span> <span data-ttu-id="44d22-105">En IIS 7, es posible que también tenga que modificar el atributo **maxAllowedContentLength** .</span><span class="sxs-lookup"><span data-stu-id="44d22-105">In IIS 7, you may also have to modify the **maxAllowedContentLength** attribute.</span></span> <span data-ttu-id="44d22-106">De forma predeterminada, el límite de carga de IIS 7 es 30 millones bytes.</span><span class="sxs-lookup"><span data-stu-id="44d22-106">By default, the IIS 7 upload limit is 30 million bytes.</span></span> <span data-ttu-id="44d22-107">Para obtener detalles e información sobre cómo cambiar el valor predeterminado de IIS, vea [KB942074](https://support.microsoft.com//kb/942074).</span><span class="sxs-lookup"><span data-stu-id="44d22-107">For details and information on changing the IIS default, see [KB942074](https://support.microsoft.com//kb/942074).</span></span>

 

 




