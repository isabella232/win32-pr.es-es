---
description: Microsoft&\# 160; El proveedor Win32 recupera y actualiza los datos relevantes para los sistemas Windows&\# 8212; datos como la configuración actual de las variables de entorno y los atributos de un disco lógico.
ms.assetid: 71c13736-0504-4d50-b8a4-5d68d4ba9a90
ms.tgt_platform: multiple
title: Proveedor Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dfb29b6f80ed833de0f4185070d46770c6cd2f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807076"
---
# <a name="win32-provider"></a><span data-ttu-id="19b55-103">Proveedor Win32</span><span class="sxs-lookup"><span data-stu-id="19b55-103">Win32 Provider</span></span>

<span data-ttu-id="19b55-104">El proveedor de Microsoft Win32 recupera y actualiza los datos relevantes para los sistemas Windows, como la configuración actual de las variables de entorno y los atributos de un disco lógico.</span><span class="sxs-lookup"><span data-stu-id="19b55-104">The Microsoft Win32 provider retrieves and updates data relevant to Windows systems—data such as the current settings of environment variables and the attributes of a logical disk.</span></span> <span data-ttu-id="19b55-105">Con el proveedor de Win32, las aplicaciones de administración pueden utilizar WMI para acceder fácilmente a estos datos.</span><span class="sxs-lookup"><span data-stu-id="19b55-105">With the Win32 provider, management applications can use WMI to easily access this data.</span></span> <span data-ttu-id="19b55-106">El proveedor Win32 recupera su información realizando llamadas a funciones de Windows y consultando el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="19b55-106">The Win32 provider retrieves its information by making Windows function calls and querying the system registry.</span></span>

<span data-ttu-id="19b55-107">El proveedor Win32 define las clases que se usan para describir el hardware o software disponible en los sistemas Windows y las relaciones entre ellos.</span><span class="sxs-lookup"><span data-stu-id="19b55-107">The Win32 provider defines the classes used to describe hardware or software available on Windows systems and the relationships between them.</span></span>

<span data-ttu-id="19b55-108">Como proveedor de instancias y métodos, el proveedor de Win32 implementa la interfaz [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) estándar, así como los siguientes métodos [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) :</span><span class="sxs-lookup"><span data-stu-id="19b55-108">As an instance and method provider, the Win32 provider implements the standard [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface as well as the following [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="19b55-109">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="19b55-109">**CreateInstanceEnumAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="19b55-110">**DeleteInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="19b55-110">**DeleteInstanceAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [<span data-ttu-id="19b55-111">**ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="19b55-111">**ExecMethodAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="19b55-112">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="19b55-112">**ExecQueryAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="19b55-113">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="19b55-113">**GetObjectAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="19b55-114">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="19b55-114">**PutInstanceAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="19b55-115">En la tabla siguiente se enumeran las categorías de clase de proveedor de Win32.</span><span class="sxs-lookup"><span data-stu-id="19b55-115">The following table lists the Win32 provider class categories.</span></span>



| <span data-ttu-id="19b55-116">Clases</span><span class="sxs-lookup"><span data-stu-id="19b55-116">Classes</span></span>                                                                             | <span data-ttu-id="19b55-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="19b55-117">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="19b55-118">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="19b55-118">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)<br/> | <span data-ttu-id="19b55-119">Objetos relacionados con el hardware.</span><span class="sxs-lookup"><span data-stu-id="19b55-119">Hardware-related objects.</span></span><br/>                                      |
| [<span data-ttu-id="19b55-120">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="19b55-120">Operating System Classes</span></span>](operating-system-classes.md)<br/>                 | <span data-ttu-id="19b55-121">Objetos relacionados con el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="19b55-121">Operating system related objects.</span></span><br/>                              |
| [<span data-ttu-id="19b55-122">Clases de contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="19b55-122">Performance Counter Classes</span></span>](performance-counter-classes.md)<br/>           | <span data-ttu-id="19b55-123">Datos de rendimiento sin procesar y calculados de los contadores de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="19b55-123">Raw and calculated performance data from performance counters.</span></span><br/> |
| [<span data-ttu-id="19b55-124">Clases de administración de servicios WMI</span><span class="sxs-lookup"><span data-stu-id="19b55-124">WMI Service Management Classes</span></span>](wmi-service-management-classes.md)<br/>     | <span data-ttu-id="19b55-125">Administración de WMI.</span><span class="sxs-lookup"><span data-stu-id="19b55-125">Management for WMI.</span></span><br/>                                            |



 

## <a name="related-topics"></a><span data-ttu-id="19b55-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="19b55-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19b55-127">Proveedor WMI de CIMWin32</span><span class="sxs-lookup"><span data-stu-id="19b55-127">CIMWin32 WMI Provider</span></span>](cimwin32-wmi-providers.md)
</dt> </dl>

 

 
