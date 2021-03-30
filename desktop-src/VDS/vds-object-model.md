---
description: Modelo de objetos de VDS
ms.assetid: e5fcc19a-e170-4918-85eb-c1457776795a
title: Modelo de objetos de VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae998955c5d0b7834cf4d88b901537f3644a2ab
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104279708"
---
# <a name="vds-object-model"></a><span data-ttu-id="9cf52-103">Modelo de objetos de VDS</span><span class="sxs-lookup"><span data-stu-id="9cf52-103">VDS Object Model</span></span>

<span data-ttu-id="9cf52-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9cf52-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="9cf52-105">VDS proporciona acceso indirecto a los dispositivos de almacenamiento basados en host, como los discos y los dispositivos de CD-ROM, y a las matrices de discos administradas por controladores RAID de hardware.</span><span class="sxs-lookup"><span data-stu-id="9cf52-105">VDS provides indirect access to host-based storage devices, such as disks and CD-ROM devices, and to disk arrays that are managed by hardware RAID controllers.</span></span> <span data-ttu-id="9cf52-106">Aunque algunas entidades de almacenamiento modelan dispositivos físicos, otras construcciones virtuales de modelo: volúmenes, particiones, etc.</span><span class="sxs-lookup"><span data-stu-id="9cf52-106">While some storage entities model physical devices, others model virtual constructs: volumes, partitions, and so on.</span></span> <span data-ttu-id="9cf52-107">Los objetos que se describen en este tema representan las entidades físicas y virtuales de VDS.</span><span class="sxs-lookup"><span data-stu-id="9cf52-107">The objects that are described in this topic represent both the physical and virtual entities of VDS.</span></span>

<span data-ttu-id="9cf52-108">Las aplicaciones llaman a los métodos expuestos por estos objetos y VDS llama al proveedor adecuado para realizar las operaciones de almacenamiento solicitadas.</span><span class="sxs-lookup"><span data-stu-id="9cf52-108">Applications call the methods that are exposed by these objects and VDS calls the appropriate provider to perform the requested storage operations.</span></span> <span data-ttu-id="9cf52-109">Una aplicación nunca llama directamente a un programa de proveedor.</span><span class="sxs-lookup"><span data-stu-id="9cf52-109">An application never calls a provider program directly.</span></span>

### <a name="classification-of-objects"></a><span data-ttu-id="9cf52-110">Clasificación de objetos</span><span class="sxs-lookup"><span data-stu-id="9cf52-110">Classification of Objects</span></span>

<span data-ttu-id="9cf52-111">Como se muestra en la siguiente ilustración, los programas de proveedor de software implementan objetos que modelan entidades basadas en host; los programas de proveedor de hardware implementan objetos que modelan dispositivos RAID de hardware interno y externo; los objetos comunes restantes son independientes del proveedor o se implementan mediante VDS.</span><span class="sxs-lookup"><span data-stu-id="9cf52-111">As the following illustration shows, software provider programs implement objects that model host-based entities; hardware provider programs implement objects that model internal and external hardware RAID devices; the remaining common objects are either provider-independent, or are implemented by VDS.</span></span> <span data-ttu-id="9cf52-112">Un eje, que no es un objeto VDS, es un término para medios de almacenamiento genéricos que constan de extensiones de disco o de unidad.</span><span class="sxs-lookup"><span data-stu-id="9cf52-112">A spindle, which is not a VDS object, is a term for generic storage media that comprises of disk or drive extents.</span></span>

![Diagrama que muestra una clasificación de objetos, definidos como ' objetos comunes ', ' objetos de proveedor de software ' y ' objetos de proveedor de hardware '.](images/vdsobjectmodel.png)

<span data-ttu-id="9cf52-114">Para obtener más información sobre el comportamiento de cada objeto, seleccione uno de los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="9cf52-114">To learn more about the behavior of each object, select from the following topics:</span></span>

-   <span data-ttu-id="9cf52-115">Los objetos de servicio y de cargador de servicio, vea [objetos de inicio y de servicio](startup-and-service-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9cf52-115">Service loader and service objects, see [Startup and Service Objects](startup-and-service-objects.md).</span></span>
-   <span data-ttu-id="9cf52-116">Enumeración y objetos Async, vea [objetos auxiliares](helper-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9cf52-116">Enumeration and async objects, see [Helper Objects](helper-objects.md).</span></span>
-   <span data-ttu-id="9cf52-117">Objeto de proveedor, consulte [objeto de proveedor](provider-object.md).</span><span class="sxs-lookup"><span data-stu-id="9cf52-117">Provider object, see [Provider Object](provider-object.md).</span></span>
-   <span data-ttu-id="9cf52-118">Paquetes, discos, volúmenes y objetos Plex de volumen, consulte [objetos de proveedor de software](software-provider-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9cf52-118">Pack, disk, volume, and volume plex objects, see [Software Provider Objects](software-provider-objects.md).</span></span>
-   <span data-ttu-id="9cf52-119">Subsistema, controlador, unidad, LUN y objetos de Plex LUN, consulte [objetos de proveedor de hardware](hardware-provider-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9cf52-119">Subsystem, controller, drive, LUN, and LUN plex objects, see [Hardware Provider Objects](hardware-provider-objects.md).</span></span>

### <a name="object-creation"></a><span data-ttu-id="9cf52-120">Creación de objetos</span><span class="sxs-lookup"><span data-stu-id="9cf52-120">Object Creation</span></span>

<span data-ttu-id="9cf52-121">La configuración y las operaciones de consulta asociadas a la creación de objetos pueden tardar un tiempo considerable en completarse; como tal, VDS invoca todos los métodos de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="9cf52-121">The configuration and query operations that are associated with object creation can take considerable time to complete; as such, VDS invokes all methods asynchronously.</span></span> <span data-ttu-id="9cf52-122">El proveedor de detección devuelve todos los eventos de finalización, error o cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="9cf52-122">The discovering provider returns all completion, error, or state change events.</span></span> <span data-ttu-id="9cf52-123">Los proveedores de software también registran todos los errores y cambios de estado significativos.</span><span class="sxs-lookup"><span data-stu-id="9cf52-123">Software providers also log all the errors and significant state changes.</span></span>

### <a name="object-deletion"></a><span data-ttu-id="9cf52-124">Eliminación del objeto</span><span class="sxs-lookup"><span data-stu-id="9cf52-124">Object Deletion</span></span>

<span data-ttu-id="9cf52-125">Varios métodos de VDS eliminan o transforman objetos VDS.</span><span class="sxs-lookup"><span data-stu-id="9cf52-125">Several VDS methods delete or transform VDS objects.</span></span> <span data-ttu-id="9cf52-126">Un llamador puede contener una referencia, por medio de un puntero de interfaz, a un objeto eliminado después de que el método devuelva.</span><span class="sxs-lookup"><span data-stu-id="9cf52-126">A caller can hold a reference, by way of an interface pointer, to a deleted object after the method returns.</span></span> <span data-ttu-id="9cf52-127">Cuando el autor de la llamada libera la interfaz, VDS elimina el objeto.</span><span class="sxs-lookup"><span data-stu-id="9cf52-127">When the caller releases the interface, VDS deletes the object.</span></span>

<span data-ttu-id="9cf52-128">En lo que respecta a la eliminación de objetos, los autores de llamadas deberían abstenerse de invocar cualquier cosa excepto el método [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="9cf52-128">With regard to object deletion, callers should refrain from invoking anything except the [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on these interfaces.</span></span> <span data-ttu-id="9cf52-129">El proveedor debe ser lo suficientemente sólido como para tratar con llamadores errantes; Si un llamador invoca un método en un objeto eliminado, el proveedor debe devolver el **\_ objeto VDS \_ E \_ eliminado**.</span><span class="sxs-lookup"><span data-stu-id="9cf52-129">The provider must be robust enough to deal with errant callers; if a caller invokes a method on a deleted object, the provider should return **VDS\_E\_OBJECT\_DELETED**.</span></span>

### <a name="service-initialization"></a><span data-ttu-id="9cf52-130">Inicialización del servicio</span><span class="sxs-lookup"><span data-stu-id="9cf52-130">Service Initialization</span></span>

<span data-ttu-id="9cf52-131">VDS proporciona un identificador de clase (CLSID) para el cargador de servicios y los objetos de servicio, pero solo el CLSID del cargador de servicios es público.</span><span class="sxs-lookup"><span data-stu-id="9cf52-131">VDS supplies a class identifier (Clsid) for the service loader and the service objects, but only the service loader Clsid is public.</span></span> <span data-ttu-id="9cf52-132">La inicialización del servicio se produce cuando los proveedores, una aplicación que llama y el servicio realizan las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="9cf52-132">Service initialization occurs when the providers, a calling application, and the service perform the following tasks:</span></span>

-   <span data-ttu-id="9cf52-133">Cada proveedor nuevo invoca el método [**IVdsAdmin:: RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) durante la instalación para registrarse con Vds.</span><span class="sxs-lookup"><span data-stu-id="9cf52-133">Each new provider invokes the [**IVdsAdmin::RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) method during installation to register with VDS.</span></span> <span data-ttu-id="9cf52-134">La llamada crea una clave del registro en el subárbol del sistema, identificada por el GUID del objeto del proveedor.</span><span class="sxs-lookup"><span data-stu-id="9cf52-134">The call creates a registry key under the SYSTEM hive, identified by the object GUID of the provider.</span></span> <span data-ttu-id="9cf52-135">En esta clave se incluye el CLSID del objeto de proveedor, el nombre, la versión y el GUID de la versión del proveedor.</span><span class="sxs-lookup"><span data-stu-id="9cf52-135">Contained under this key is the Clsid of the provider object, the name, version, and the version GUID of the provider.</span></span>
    > [!Note]  
    > <span data-ttu-id="9cf52-136">Los GUID del objeto de proveedor son persistentes; no se admiten los GUID de objetos de software y hardware.</span><span class="sxs-lookup"><span data-stu-id="9cf52-136">Provider object GUIDs are persistent; software and hardware object GUIDs are not.</span></span>

     

-   <span data-ttu-id="9cf52-137">Una aplicación llama a la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y pasa el CLSID del cargador de servicios como argumento.</span><span class="sxs-lookup"><span data-stu-id="9cf52-137">An application calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function, passing the service loader Clsid as an argument.</span></span> <span data-ttu-id="9cf52-138">Con un puntero al objeto de cargador de servicio, la aplicación puede iniciar VDS localmente o de forma remota pasando el nombre de equipo deseado como parámetro al método [**IVdsServiceLoader:: LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) .</span><span class="sxs-lookup"><span data-stu-id="9cf52-138">With a pointer to the service loader object, the application can start VDS either locally or remotely by passing the desired computer name as a parameter to the [**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) method.</span></span>
-   <span data-ttu-id="9cf52-139">Cuando la aplicación inicial se asocia al servicio, VDS llama primero a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en cada CLSID que se encuentra en la clave del registro y, a continuación, llama al método [**IVdsProviderPrivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) en cada proveedor para inicializar los programas.</span><span class="sxs-lookup"><span data-stu-id="9cf52-139">When the initial application attaches to the service, VDS first calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on each Clsid found under the registry key, and then calls the [**IVdsProviderPrivate::OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) method on each provider to initialize the programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cf52-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9cf52-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cf52-141">Acerca de VDS</span><span class="sxs-lookup"><span data-stu-id="9cf52-141">About VDS</span></span>](about-vds.md)
</dt> <dt>

[<span data-ttu-id="9cf52-142">**IVdsAdmin:: RegisterProvider**</span><span class="sxs-lookup"><span data-stu-id="9cf52-142">**IVdsAdmin::RegisterProvider**</span></span>](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider)
</dt> <dt>

[<span data-ttu-id="9cf52-143">**IVdsServiceLoader::LoadService**</span><span class="sxs-lookup"><span data-stu-id="9cf52-143">**IVdsServiceLoader::LoadService**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[<span data-ttu-id="9cf52-144">**IVdsProviderPrivate:: OnLoad**</span><span class="sxs-lookup"><span data-stu-id="9cf52-144">**IVdsProviderPrivate::OnLoad**</span></span>](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> </dl>

 

 
