---
description: El servicio de disco virtual (VDS) administra una amplia gama de configuraciones de almacenamiento, desde escritorios de un solo disco hasta matrices de almacenamiento externo. El servicio expone una interfaz de programación de aplicaciones (API).
ms.assetid: 536aafd2-cc04-48cc-8ee7-920efbba2a5f
title: Servicio de disco virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcfef0c5a73fcb2e6911395c829380c4bdfe56ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677931"
---
# <a name="virtual-disk-service"></a><span data-ttu-id="a2ccd-104">Servicio de disco virtual</span><span class="sxs-lookup"><span data-stu-id="a2ccd-104">Virtual Disk Service</span></span>

<span data-ttu-id="a2ccd-105">\[A partir de Windows 8 y Windows Server 2012, la interfaz COM de servicio de disco virtual se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a2ccd-105">\[Beginning with Windows 8 and Windows Server 2012, the Virtual Disk Service COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

## <a name="purpose"></a><span data-ttu-id="a2ccd-106">Propósito</span><span class="sxs-lookup"><span data-stu-id="a2ccd-106">Purpose</span></span>

<span data-ttu-id="a2ccd-107">El servicio de disco virtual (VDS) administra una amplia gama de configuraciones de almacenamiento, desde escritorios de un solo disco hasta matrices de almacenamiento externo.</span><span class="sxs-lookup"><span data-stu-id="a2ccd-107">The Virtual Disk Service (VDS) manages a wide range of storage configurations, from single-disk desktops to external storage arrays.</span></span> <span data-ttu-id="a2ccd-108">El servicio expone una interfaz de programación de aplicaciones (API).</span><span class="sxs-lookup"><span data-stu-id="a2ccd-108">The service exposes an application programming interface (API).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="a2ccd-109">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="a2ccd-109">Where applicable</span></span>

<span data-ttu-id="a2ccd-110">A partir de Windows 8 y Windows Server 8, la interfaz COM de servicio de disco virtual se sustituye por la API de administración de almacenamiento, una interfaz de programación basada en WMI.</span><span class="sxs-lookup"><span data-stu-id="a2ccd-110">Beginning with Windows 8 and Windows Server 8, the Virtual Disk Service COM interface is superseded by the Storage Management API, a WMI-based programming interface.</span></span> <span data-ttu-id="a2ccd-111">Para administrar los subsistemas de almacenamiento, los discos, las particiones y los volúmenes de (Windows), se recomienda encarecidamente usar la API de administración de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="a2ccd-111">For managing storage subsystems, (Windows) disks, partitions, and volumes, we strongly recommend using the Storage Management API.</span></span> <span data-ttu-id="a2ccd-112">Para obtener más información, consulte la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).</span><span class="sxs-lookup"><span data-stu-id="a2ccd-112">For more information, see the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).</span></span>

<span data-ttu-id="a2ccd-113">En el caso de todos los usos excepto los volúmenes de arranque reflejado (mediante un volumen reflejado para hospedar el sistema operativo), los discos dinámicos están desusados.</span><span class="sxs-lookup"><span data-stu-id="a2ccd-113">For all usages except mirror boot volumes (using a mirror volume to host the operating system ), dynamic disks are deprecated.</span></span> <span data-ttu-id="a2ccd-114">En el caso de los datos que requieren resistencia frente a errores de unidad, use espacios de almacenamiento, una solución de virtualización de almacenamiento resistente.</span><span class="sxs-lookup"><span data-stu-id="a2ccd-114">For data that requires resiliency against drive failure, use Storage Spaces, a resilient storage virtualization solution.</span></span> <span data-ttu-id="a2ccd-115">Para obtener más información, consulte la [vista previa técnica de espacios de almacenamiento](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="a2ccd-115">For more information, see [Storage Spaces Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).</span></span>

<span data-ttu-id="a2ccd-116">Los desarrolladores de aplicaciones que usan las interfaces descritas en esta guía pueden consultar y configurar un conjunto heterogéneo de almacenamiento administrado internamente y proporcionado por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="a2ccd-116">Application developers who use the interfaces described in this guide can query and configure a heterogeneous set of vendor-supplied and internally managed storage.</span></span> <span data-ttu-id="a2ccd-117">VDS oculta de las aplicaciones las complejidades asociadas con el almacenamiento, lo que permite que el servicio sea independiente del proveedor y de la tecnología.</span><span class="sxs-lookup"><span data-stu-id="a2ccd-117">VDS hides from applications the complexities associated with storage, making the service both vendor and technology neutral.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a2ccd-118">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="a2ccd-118">Developer audience</span></span>

<span data-ttu-id="a2ccd-119">Esta documentación está destinada a los desarrolladores de aplicaciones que están familiarizados con las capacidades de almacenamiento de las plataformas de Microsoft Windows y que conocen el desarrollo COM.</span><span class="sxs-lookup"><span data-stu-id="a2ccd-119">This documentation is intended for application developers who are familiar with the storage capabilities of Microsoft Windows platforms and who are knowledgeable about COM development.</span></span>

<span data-ttu-id="a2ccd-120">La guía también está destinada a los fabricantes de subsistemas de hardware que desarrollan y admiten programas de proveedor de hardware VDS.</span><span class="sxs-lookup"><span data-stu-id="a2ccd-120">The guide is also intended for hardware subsystem manufacturers who develop and support VDS hardware provider programs.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a2ccd-121">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="a2ccd-121">Run-time requirements</span></span>

<span data-ttu-id="a2ccd-122">VDS es compatible con Windows Server 2003, Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a2ccd-122">VDS is supported on Windows Server 2003, Windows Vista, and later.</span></span> <span data-ttu-id="a2ccd-123">Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación determinado, consulte la sección de requisitos de la documentación de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="a2ccd-123">For information about run-time requirements for a particular programming element, see the Requirements section of the documentation for that element.</span></span>

<span data-ttu-id="a2ccd-124">Se admite la ejecución de aplicaciones VDS de 32 bits en WOW64, pero los proveedores de VDS de 64 bits deben ejecutarse como aplicaciones nativas en versiones de Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a2ccd-124">Running 32-bit VDS applications under WOW64 is supported, but 64-bit VDS providers must run as native applications on 64-bit Windows versions.</span></span>

<span data-ttu-id="a2ccd-125">VDS está disponible en el kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a2ccd-125">VDS is available in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a2ccd-126">Puede instalar el SDK para Windows 7 y Windows Server 2008 R2 desde el [centro de descarga de Windows](https://www.microsoft.com/download/details.aspx?id=8279).</span><span class="sxs-lookup"><span data-stu-id="a2ccd-126">You can install the SDK for Windows 7 and Windows Server 2008 R2 from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span> <span data-ttu-id="a2ccd-127">Esta versión del Windows SDK se puede usar para desarrollar aplicaciones de VDS para Windows Server 2003, Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a2ccd-127">This version of the Windows SDK can be used to develop VDS applications for Windows Server 2003, Windows Vista, and later.</span></span> <span data-ttu-id="a2ccd-128">También puede descargar la [versión ISO](https://www.microsoft.com/download/details.aspx?id=8442) del SDK desde el centro de descarga de Windows.</span><span class="sxs-lookup"><span data-stu-id="a2ccd-128">You can also download the [ISO version](https://www.microsoft.com/download/details.aspx?id=8442) of the SDK from the Windows Download Center.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a2ccd-129">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a2ccd-129">In this section</span></span>



| <span data-ttu-id="a2ccd-130">Tema</span><span class="sxs-lookup"><span data-stu-id="a2ccd-130">Topic</span></span>                                         | <span data-ttu-id="a2ccd-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2ccd-131">Description</span></span>                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2ccd-132">Acerca de VDS</span><span class="sxs-lookup"><span data-stu-id="a2ccd-132">About VDS</span></span>](about-vds.md)<br/>         | <span data-ttu-id="a2ccd-133">Describe el modelo de objetos VDS, las estrategias de configuración de almacenamiento y las notificaciones de VDS.</span><span class="sxs-lookup"><span data-stu-id="a2ccd-133">Describes the VDS object model, storage-configuration strategies, and VDS notifications.</span></span><br/>    |
| [<span data-ttu-id="a2ccd-134">Uso de VDS</span><span class="sxs-lookup"><span data-stu-id="a2ccd-134">Using VDS</span></span>](using-vds.md)<br/>         | <span data-ttu-id="a2ccd-135">Describe cómo usar VDS para consultar y configurar dispositivos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="a2ccd-135">Describes how to use VDS to query and configure storage devices.</span></span><br/>                            |
| [<span data-ttu-id="a2ccd-136">Referencia de VDS</span><span class="sxs-lookup"><span data-stu-id="a2ccd-136">VDS Reference</span></span>](vds-reference.md)<br/> | <span data-ttu-id="a2ccd-137">Describe las constantes de VDS, los tipos de datos, las enumeraciones, las interfaces, las estructuras y los códigos de error.</span><span class="sxs-lookup"><span data-stu-id="a2ccd-137">Describes VDS constants, data types, enumerations, interfaces, structures, and error codes.</span></span><br/> |



 

 

