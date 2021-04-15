---
description: Agregar una letra de unidad a un LUN
ms.assetid: 3f350312-3f1f-4020-90d0-85521ea9c7c8
title: Agregar una letra de unidad a un LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426a4f3bf720b21a02462edde4a381012d2084d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696314"
---
# <a name="adding-a-drive-letter-to-a-lun"></a><span data-ttu-id="d978e-103">Agregar una letra de unidad a un LUN</span><span class="sxs-lookup"><span data-stu-id="d978e-103">Adding a Drive Letter to a LUN</span></span>

<span data-ttu-id="d978e-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d978e-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="d978e-105">Puede asignar Letras de unidad a objetos de volumen directamente. sin embargo, si el disco es un objeto LUN, tendrá algunos pasos adicionales.</span><span class="sxs-lookup"><span data-stu-id="d978e-105">You can assign drive letters to volume objects directly; however, if your disk is a LUN object, you have a few additional steps.</span></span>

<span data-ttu-id="d978e-106">**Para asignar una letra de unidad a un objeto LUN**</span><span class="sxs-lookup"><span data-stu-id="d978e-106">**To assign a drive letter to a LUN object**</span></span>

1.  <span data-ttu-id="d978e-107">Si es necesario, desenmascarar el LUN en el host local.</span><span class="sxs-lookup"><span data-stu-id="d978e-107">If necessary, unmask the LUN to the local host.</span></span>
    > [!Note]  
    > <span data-ttu-id="d978e-108">No se pueden realizar operaciones administrativas de software en un objeto LUN sin máscara en otro equipo dentro de la sesión actual de VDS.</span><span class="sxs-lookup"><span data-stu-id="d978e-108">You cannot perform software administrative operations on a LUN object that is unmasked to another computer within the current VDS session.</span></span>

     

2.  <span data-ttu-id="d978e-109">Invoque el método [**IVdsService:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) en el equipo que ejecuta el proveedor de hardware.</span><span class="sxs-lookup"><span data-stu-id="d978e-109">Invoke the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method on the computer that is running the hardware provider.</span></span>
3.  <span data-ttu-id="d978e-110">Inicialice el LUN como un disco básico de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d978e-110">Initialize the LUN as a basic disk as follows:</span></span>
    1.  <span data-ttu-id="d978e-111">Invoque el método [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el objeto LUN para consultar la interfaz [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) .</span><span class="sxs-lookup"><span data-stu-id="d978e-111">Invoke the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the LUN object to query for the [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) interface.</span></span>
    2.  <span data-ttu-id="d978e-112">Invoque el método [**IVdsSwProvider:: CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) para crear un paquete básico.</span><span class="sxs-lookup"><span data-stu-id="d978e-112">Invoke the [**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) method to create a basic pack.</span></span>
    3.  <span data-ttu-id="d978e-113">Invoque el método [**IVdsPack:: AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) para agregar el disco al nuevo paquete.</span><span class="sxs-lookup"><span data-stu-id="d978e-113">Invoke the [**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) method to add the disk to the new pack.</span></span>
4.  <span data-ttu-id="d978e-114">Cree una partición en el disco y obtenga el objeto de volumen como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="d978e-114">Create a partition on the disk and obtain the volume object as follows:</span></span>
    1.  <span data-ttu-id="d978e-115">Invoque el método [**IVdsCreatePartitionEx:: CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) para crear una partición.</span><span class="sxs-lookup"><span data-stu-id="d978e-115">Invoke the [**IVdsCreatePartitionEx::CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) method to create a partition.</span></span>
    2.  <span data-ttu-id="d978e-116">Invoque el método [**IVdsAsync:: wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) en el objeto asincrónico devuelto por [**CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) para obtener el identificador de volumen de la estructura de [**\_ \_ salida asincrónica de VDS**](/windows/desktop/api/Vds/ns-vds-vds_async_output) .</span><span class="sxs-lookup"><span data-stu-id="d978e-116">Invoke the [**IVdsAsync::Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) method on the async object that is returned by [**CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) to get the volume identifier from the [**VDS\_ASYNC\_OUTPUT**](/windows/desktop/api/Vds/ns-vds-vds_async_output) structure.</span></span>
    3.  <span data-ttu-id="d978e-117">Pase el identificador de volumen como parámetro al método [**IVdsService:: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) para obtener un puntero de objeto de volumen.</span><span class="sxs-lookup"><span data-stu-id="d978e-117">Pass the volume identifier as a parameter to the [**IVdsService::GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) method to get a volume object pointer.</span></span>
5.  <span data-ttu-id="d978e-118">Invoque el método [**IVdsVolumeMF:: AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) para asignar la letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="d978e-118">Invoke the [**IVdsVolumeMF::AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) method to assign the drive letter.</span></span>

> [!Note]  
> <span data-ttu-id="d978e-119">El método [**IVdsAdvancedDisk:: AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) asigna las letras de unidad a las particiones sin volúmenes asociados, como las particiones OEM o ESP.</span><span class="sxs-lookup"><span data-stu-id="d978e-119">The [**IVdsAdvancedDisk::AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) method assigns drive letters to partitions without associated volumes, such as OEM or ESP partitions.</span></span> <span data-ttu-id="d978e-120">No se puede usar para asignar una letra de unidad a un objeto LUN.</span><span class="sxs-lookup"><span data-stu-id="d978e-120">You cannot use it to assign a drive letter to a LUN object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d978e-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d978e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d978e-122">Uso de VDS</span><span class="sxs-lookup"><span data-stu-id="d978e-122">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="d978e-123">**IVdsService:: reenumerar**</span><span class="sxs-lookup"><span data-stu-id="d978e-123">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="d978e-124">**IVdsDisk**</span><span class="sxs-lookup"><span data-stu-id="d978e-124">**IVdsDisk**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[<span data-ttu-id="d978e-125">**IVdsSwProvider::CreatePack**</span><span class="sxs-lookup"><span data-stu-id="d978e-125">**IVdsSwProvider::CreatePack**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[<span data-ttu-id="d978e-126">**IVdsPack::AddDisk**</span><span class="sxs-lookup"><span data-stu-id="d978e-126">**IVdsPack::AddDisk**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> <dt>

[<span data-ttu-id="d978e-127">**IVdsCreatePartitionEx::CreatePartitionEx**</span><span class="sxs-lookup"><span data-stu-id="d978e-127">**IVdsCreatePartitionEx::CreatePartitionEx**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex)
</dt> <dt>

[<span data-ttu-id="d978e-128">**IVdsAsync:: wait**</span><span class="sxs-lookup"><span data-stu-id="d978e-128">**IVdsAsync::Wait**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[<span data-ttu-id="d978e-129">**\_salida asincrónica de VDS \_**</span><span class="sxs-lookup"><span data-stu-id="d978e-129">**VDS\_ASYNC\_OUTPUT**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_async_output)
</dt> <dt>

[<span data-ttu-id="d978e-130">**IVdsVolumeMF::AddAccessPath**</span><span class="sxs-lookup"><span data-stu-id="d978e-130">**IVdsVolumeMF::AddAccessPath**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath)
</dt> <dt>

[<span data-ttu-id="d978e-131">**IVdsAdvancedDisk::AssignDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="d978e-131">**IVdsAdvancedDisk::AssignDriveLetter**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter)
</dt> </dl>

 

 
