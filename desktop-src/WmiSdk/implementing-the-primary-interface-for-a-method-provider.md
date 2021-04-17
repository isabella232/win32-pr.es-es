---
description: 'Un proveedor de métodos debe implementar IWbemServices como la interfaz principal. Sin embargo, un proveedor de método puro solo requiere que se implemente el método IWbemServices:: ExecMethodAsync.'
ms.assetid: 39466513-48f3-4bf6-a3ab-e9d2c387480c
ms.tgt_platform: multiple
title: Implementar la interfaz principal para un proveedor de métodos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 196f87a6520d92bf18362be88f8cc40e5133dabe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706757"
---
# <a name="implementing-the-primary-interface-for-a-method-provider"></a><span data-ttu-id="8fb61-104">Implementar la interfaz principal para un proveedor de métodos</span><span class="sxs-lookup"><span data-stu-id="8fb61-104">Implementing the Primary Interface for a Method Provider</span></span>

<span data-ttu-id="8fb61-105">Un proveedor de métodos debe implementar [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) como la interfaz principal.</span><span class="sxs-lookup"><span data-stu-id="8fb61-105">A method provider should implement [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface.</span></span> <span data-ttu-id="8fb61-106">Sin embargo, un proveedor de método puro solo requiere que se implemente el método [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) .</span><span class="sxs-lookup"><span data-stu-id="8fb61-106">However, a pure method provider requires only that you implement the [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) method.</span></span>

<span data-ttu-id="8fb61-107">Dado que otros proveedores usan [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), la interfaz contiene muchos métodos que son irrelevantes para un proveedor de métodos puros.</span><span class="sxs-lookup"><span data-stu-id="8fb61-107">Because other providers use [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), the interface contains many methods that are irrelevant to a pure method provider.</span></span> <span data-ttu-id="8fb61-108">El proveedor de método puro debe proporcionar una implementación de código auxiliar que devuelva el \_ proveedor WBEM E \_ \_ no \_ sea compatible con todos los demás métodos **IWbemServices** además de [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span><span class="sxs-lookup"><span data-stu-id="8fb61-108">Your pure method provider should supply a stub implementation that returns WBEM\_E\_PROVIDER\_NOT\_CAPABLE for all of other **IWbemServices** methods besides [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span></span> <span data-ttu-id="8fb61-109">Sin embargo, muchos proveedores de métodos también sirven como proveedores de instancias o de clases.</span><span class="sxs-lookup"><span data-stu-id="8fb61-109">However, many method providers also serve as instance or class providers.</span></span> <span data-ttu-id="8fb61-110">Los proveedores de instancias y métodos combinados deben admitir más métodos **IWbemServices** .</span><span class="sxs-lookup"><span data-stu-id="8fb61-110">Combination method and instance providers must support more of the **IWbemServices** methods.</span></span>

 

 



