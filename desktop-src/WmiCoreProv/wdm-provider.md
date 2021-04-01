---
description: El proveedor WDM (Modelo de controlador de Windows) concede acceso a las clases, instancias, métodos y eventos de los controladores de hardware que se ajustan al modelo WDM.
ms.assetid: 2f9749ff-b318-4228-80fd-e3846dde21d2
title: Proveedor de WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d96ce356214f2788d3608b2ba85943e607394cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811432"
---
# <a name="wdm-provider"></a><span data-ttu-id="5f31e-103">Proveedor de WDM</span><span class="sxs-lookup"><span data-stu-id="5f31e-103">WDM Provider</span></span>

<span data-ttu-id="5f31e-104">El proveedor WDM (Modelo de controlador de Windows) concede acceso a las clases, instancias, métodos y eventos de los controladores de hardware que se ajustan al modelo WDM.</span><span class="sxs-lookup"><span data-stu-id="5f31e-104">The WDM (Windows Driver Model) provider grants access to the classes, instances, methods, and events of hardware drivers that conform to the WDM model.</span></span> <span data-ttu-id="5f31e-105">Las clases para los controladores de hardware residen en el " \\ espacio de nombres WMI raíz".</span><span class="sxs-lookup"><span data-stu-id="5f31e-105">The classes for hardware drivers reside in the "root\\wmi namespace".</span></span>

<span data-ttu-id="5f31e-106">Las clases WDM se definen principalmente en WMI. mof.</span><span class="sxs-lookup"><span data-stu-id="5f31e-106">WDM classes are defined primarily in Wmi.mof.</span></span>

<span data-ttu-id="5f31e-107">WDM es una interfaz del sistema operativo a través de la cual los componentes de hardware proporcionan información y notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="5f31e-107">WDM is an operating system interface through which hardware components provide information and event notification.</span></span> <span data-ttu-id="5f31e-108">El proveedor de WDM es una clase, una instancia, un evento y un proveedor de métodos que permite a las aplicaciones de administración tener acceso a los datos y eventos de los controladores de dispositivos habilitados para WMI para WDM.</span><span class="sxs-lookup"><span data-stu-id="5f31e-108">The WDM provider is a class, instance, event, and method provider that allows management applications access to data and events from WMI-for-WDM enabled device drivers.</span></span> <span data-ttu-id="5f31e-109">Las clases creadas por el proveedor WDM para representar los datos del controlador de dispositivo solo se encuentran en el espacio de nombres "raíz de \\ WMI".</span><span class="sxs-lookup"><span data-stu-id="5f31e-109">The classes created by the WDM provider to represent device driver data reside only in the "Root\\WMI" namespace.</span></span> <span data-ttu-id="5f31e-110">Este espacio de nombres ya debe existir antes de que el proveedor de WDM procese los controladores WDM instalados.</span><span class="sxs-lookup"><span data-stu-id="5f31e-110">This namespace must already exist before the WDM provider will process the installed WDM drivers.</span></span>

<span data-ttu-id="5f31e-111">El proveedor de WDM registra información acerca de las operaciones WDM en el archivo WmiProv. log.</span><span class="sxs-lookup"><span data-stu-id="5f31e-111">The WDM provider records information about WDM operations in the WmiProv.log file.</span></span> <span data-ttu-id="5f31e-112">Para obtener más información, consulte [archivos de registro de WMI](/windows/desktop/WmiSdk/wmi-log-files).</span><span class="sxs-lookup"><span data-stu-id="5f31e-112">For more information, see [WMI Log Files](/windows/desktop/WmiSdk/wmi-log-files).</span></span>

<span data-ttu-id="5f31e-113">Como una clase, una instancia, un método y un proveedor de eventos, el proveedor WDM implementa la interfaz [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) estándar, así como los siguientes métodos [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) :</span><span class="sxs-lookup"><span data-stu-id="5f31e-113">As a class, instance, method, and event provider, the WDM provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the following [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="5f31e-114">**CreateClassEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="5f31e-114">**CreateClassEnumAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [<span data-ttu-id="5f31e-115">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="5f31e-115">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="5f31e-116">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="5f31e-116">**GetObjectAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="5f31e-117">**ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="5f31e-117">**ExecMethodAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="5f31e-118">**ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="5f31e-118">**ExecNotificationQueryAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [<span data-ttu-id="5f31e-119">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="5f31e-119">**ExecQueryAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="5f31e-120">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="5f31e-120">**PutInstanceAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="5f31e-121">El proveedor WDM admite el evento extrínseco de [**WMIEvent**](/windows/desktop/WmiCoreProv/wmievent) , que notifica a WMI los eventos de los controladores basados en WDM.</span><span class="sxs-lookup"><span data-stu-id="5f31e-121">The WDM provider supports the [**WMIEvent**](/windows/desktop/WmiCoreProv/wmievent) extrinsic event, which notifies WMI regarding events from WDM-based drivers.</span></span> <span data-ttu-id="5f31e-122">Puede registrar los consumidores de eventos para los eventos de **WMIEvent** como lo haría con cualquier otro evento.</span><span class="sxs-lookup"><span data-stu-id="5f31e-122">You can register your event consumers for **WMIEvent** events as you would any other event.</span></span> <span data-ttu-id="5f31e-123">Para obtener más información, consulte [recibir un evento WMI](/windows/desktop/WmiSdk/receiving-a-wmi-event).</span><span class="sxs-lookup"><span data-stu-id="5f31e-123">For more information, see [Receiving a WMI Event](/windows/desktop/WmiSdk/receiving-a-wmi-event).</span></span> <span data-ttu-id="5f31e-124">No se generan eventos de creación de clase al iniciar un controlador.</span><span class="sxs-lookup"><span data-stu-id="5f31e-124">No class creation events are raised when starting a driver.</span></span>

<span data-ttu-id="5f31e-125">El proveedor WDM es compatible con la clase siguiente:</span><span class="sxs-lookup"><span data-stu-id="5f31e-125">The WDM provider supports the following class:</span></span>

-   [<span data-ttu-id="5f31e-126">**WMIBinaryMofResource**</span><span class="sxs-lookup"><span data-stu-id="5f31e-126">**WMIBinaryMofResource**</span></span>](wmibinarymofresource.md)

## <a name="related-topics"></a><span data-ttu-id="5f31e-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5f31e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f31e-128">Proveedores WMI</span><span class="sxs-lookup"><span data-stu-id="5f31e-128">WMI Providers</span></span>](/windows/desktop/WmiSdk/wmi-providers)
</dt> <dt>

[<span data-ttu-id="5f31e-129">Acceder a los datos desde los controladores de dispositivos</span><span class="sxs-lookup"><span data-stu-id="5f31e-129">Accessing Data from Device Drivers</span></span>](/windows/desktop/WmiSdk/accessing-data-from-device-drivers)
</dt> </dl>

 

 
