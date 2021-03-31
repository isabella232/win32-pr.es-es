---
description: Un proveedor de alto rendimiento de WMI aumenta en gran medida la velocidad a la que un cliente WMI puede obtener información de un proveedor de instancias WMI.
ms.assetid: 767a16bb-44b6-4c56-b79b-23241fcc216e
ms.tgt_platform: multiple
title: Mejorar la eficacia de un proveedor de instancias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fecd0d8a20a3dcccd2878996823a7eb8a7ec0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911502"
---
# <a name="improving-the-efficiency-of-an-instance-provider"></a><span data-ttu-id="bfe4e-103">Mejorar la eficacia de un proveedor de instancias</span><span class="sxs-lookup"><span data-stu-id="bfe4e-103">Improving the Efficiency of an Instance Provider</span></span>

<span data-ttu-id="bfe4e-104">Un proveedor de alto rendimiento de WMI aumenta en gran medida la velocidad a la que un cliente WMI puede obtener información de un proveedor de instancias WMI.</span><span class="sxs-lookup"><span data-stu-id="bfe4e-104">A WMI high-performance provider greatly increases the speed at which a WMI client can obtain information from a WMI instance provider.</span></span> <span data-ttu-id="bfe4e-105">El cambio principal es que un proveedor de alto rendimiento se ejecuta como un servidor en proceso en la aplicación cliente o en WMI.</span><span class="sxs-lookup"><span data-stu-id="bfe4e-105">The main change is that a high-performance provider runs as an in-process server to either the client application or to WMI.</span></span> <span data-ttu-id="bfe4e-106">Al colocar el proveedor en el proceso del cliente, puede acelerar la interacción entre los dos.</span><span class="sxs-lookup"><span data-stu-id="bfe4e-106">By placing the provider inside the client process, you can speed up the interaction between the two.</span></span>

<span data-ttu-id="bfe4e-107">Para obtener más información sobre cómo convertir un proveedor de instancias en un proveedor de alto rendimiento, vea [crear un proveedor de instancias en un proveedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="bfe4e-107">For more information about how to make your instance provider a high-performance provider, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md).</span></span>

 

 



