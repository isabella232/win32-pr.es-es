---
description: El proveedor de vistas es una instancia y un proveedor de métodos que crea nuevas clases basadas en instancias de otras clases.
ms.assetid: e1992e10-647b-4747-8f3d-b437ef7f3770
ms.tgt_platform: multiple
title: Ver proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e49154504dfb2f71ec19c2275851befbdbf9a48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911481"
---
# <a name="view-provider"></a><span data-ttu-id="b2a63-103">Ver proveedor</span><span class="sxs-lookup"><span data-stu-id="b2a63-103">View Provider</span></span>

<span data-ttu-id="b2a63-104">El proveedor de vistas es una instancia y un proveedor de métodos que crea nuevas clases basadas en instancias de otras clases.</span><span class="sxs-lookup"><span data-stu-id="b2a63-104">The View provider is an instance and method provider that creates new classes based on instances of other classes.</span></span> <span data-ttu-id="b2a63-105">Puede usar el proveedor de vistas para tomar propiedades de diferentes clases de origen, espacios de nombres diferentes o equipos diferentes y combinar las propiedades como una sola clase.</span><span class="sxs-lookup"><span data-stu-id="b2a63-105">You can use the View provider to take properties from different source classes, different namespaces, or different computers and combine the properties as a single class.</span></span>

<span data-ttu-id="b2a63-106">Como proveedor de instancias y métodos, el proveedor de vistas admite la interfaz estándar [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) y los siguientes métodos [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) :</span><span class="sxs-lookup"><span data-stu-id="b2a63-106">As an instance and method provider, the View provider supports the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface and the following [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="b2a63-107">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="b2a63-107">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="b2a63-108">**ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="b2a63-108">**ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="b2a63-109">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="b2a63-109">**ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="b2a63-110">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="b2a63-110">**GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="b2a63-111">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="b2a63-111">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="b2a63-112">Para obtener más información sobre los calificadores que se usan para definir las clases de proveedor de vistas, vea [calificadores específicos del proveedor de vistas](qualifiers-specific-to-the-view-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b2a63-112">For more information about the qualifiers use to define View provider classes, see [Qualifiers Specific to the View Provider](qualifiers-specific-to-the-view-provider.md).</span></span>

<span data-ttu-id="b2a63-113">Para obtener más información acerca de las vistas, vea [vincular clases juntas](linking-classes-together.md).</span><span class="sxs-lookup"><span data-stu-id="b2a63-113">For more information about views, see [Linking Classes Together](linking-classes-together.md).</span></span>

<span data-ttu-id="b2a63-114">Dos versiones del proveedor de vistas están disponibles en las plataformas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b2a63-114">Two versions of the View provider are available on 64-bit platforms.</span></span> <span data-ttu-id="b2a63-115">Para obtener más información, consulte [obtener y proporcionar datos en un equipo de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md).</span><span class="sxs-lookup"><span data-stu-id="b2a63-115">For more information, see [Getting and Providing Data on a 64-bit Computer](getting-and-providing-data-on-a-64-bit-computer.md).</span></span>

<span data-ttu-id="b2a63-116">El proveedor de vistas se implementa en ViewProv.dll.</span><span class="sxs-lookup"><span data-stu-id="b2a63-116">The View provider is implemented in ViewProv.dll.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2a63-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b2a63-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2a63-118">Proveedores WMI</span><span class="sxs-lookup"><span data-stu-id="b2a63-118">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 



