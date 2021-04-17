---
description: Objeto de destino
ms.assetid: e88d65ad-9b56-4620-a0f5-573c5e245b3e
title: Objeto de destino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1e81ea94a2f608378eba069defc83a721e0fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697687"
---
# <a name="target-object"></a><span data-ttu-id="77d5c-103">Objeto de destino</span><span class="sxs-lookup"><span data-stu-id="77d5c-103">Target Object</span></span>

<span data-ttu-id="77d5c-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="77d5c-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="77d5c-105">Un objeto de destino modela un destino iSCSI que está incluido en un subsistema iSCSI.</span><span class="sxs-lookup"><span data-stu-id="77d5c-105">A target object models an iSCSI target that is contained within an iSCSI subsystem.</span></span>

<span data-ttu-id="77d5c-106">Use el método [**IVdsSubSystemIscsi:: QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) para determinar los destinos iSCSI del subsistema.</span><span class="sxs-lookup"><span data-stu-id="77d5c-106">Use the [**IVdsSubSystemIscsi::QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) method to determine the iSCSI targets of the subsystem.</span></span> <span data-ttu-id="77d5c-107">Los llamadores pueden obtener un puntero a un destino específico seleccionando el objeto de destino deseado de la enumeración devuelta por el método **QueryTargets** .</span><span class="sxs-lookup"><span data-stu-id="77d5c-107">Callers can get a pointer to a specific target by selecting the desired target object from the enumeration that is returned by the **QueryTargets** method.</span></span> <span data-ttu-id="77d5c-108">Con un objeto de destino, puede establecer el nombre descriptivo y la consulta del destino para las propiedades de destino, los LUN asociados y el subsistema que contiene el destino.</span><span class="sxs-lookup"><span data-stu-id="77d5c-108">With a target object, you can set the target's friendly name and query for target properties, associated LUNs, and the subsystem that contains the target.</span></span>

<span data-ttu-id="77d5c-109">Los equipos host deben iniciar sesión en los destinos para tener acceso a los LUN asociados.</span><span class="sxs-lookup"><span data-stu-id="77d5c-109">Host computers must log on to targets to access their associated LUNs.</span></span> <span data-ttu-id="77d5c-110">Para realizar un inicio de sesión en un destino, el destino debe tener al menos un portal asociado en uno de sus grupos de portal.</span><span class="sxs-lookup"><span data-stu-id="77d5c-110">To perform a logon to a target, the target must have at least one associated portal in one of its portal groups.</span></span> <span data-ttu-id="77d5c-111">La entrada y la salida de los LUN asociados se administran a través de esta sesión de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="77d5c-111">Input to and output from associated LUNs is handled through this logon session.</span></span>

<span data-ttu-id="77d5c-112">Las propiedades del objeto de destino incluyen un identificador de objeto, un nombre iSCSI, un nombre descriptivo y una marca habilitada para CHAP.</span><span class="sxs-lookup"><span data-stu-id="77d5c-112">Target object properties include an object identifier, an iSCSI name, a friendly name, and a CHAP-enabled flag.</span></span>

<span data-ttu-id="77d5c-113">En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.</span><span class="sxs-lookup"><span data-stu-id="77d5c-113">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="77d5c-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="77d5c-114">Type</span></span>                                                                                      | <span data-ttu-id="77d5c-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="77d5c-115">Element</span></span>                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77d5c-116">Interfaces que siempre expone este objeto en los proveedores iSCSI de VDS 1,1 y 2,0</span><span class="sxs-lookup"><span data-stu-id="77d5c-116">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="77d5c-117">[**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).</span><span class="sxs-lookup"><span data-stu-id="77d5c-117">[**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).</span></span>                                                                                 |
| <span data-ttu-id="77d5c-118">Enumeraciones asociadas</span><span class="sxs-lookup"><span data-stu-id="77d5c-118">Associated enumerations</span></span>                                                                   | <span data-ttu-id="77d5c-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="77d5c-119">None.</span></span>                                                                                                                       |
| <span data-ttu-id="77d5c-120">Estructuras asociadas</span><span class="sxs-lookup"><span data-stu-id="77d5c-120">Associated structures</span></span>                                                                     | <span data-ttu-id="77d5c-121">[**VDS \_ \_ \_ Propuesta de destino iSCSI**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) y [**\_ \_ notificación de destino de VDS**](/windows/desktop/api/Vds/ns-vds-vds_target_notification).</span><span class="sxs-lookup"><span data-stu-id="77d5c-121">[**VDS\_ISCSI\_TARGET\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) and [**VDS\_TARGET\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_target_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="77d5c-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77d5c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77d5c-123">Objetos de proveedor de hardware</span><span class="sxs-lookup"><span data-stu-id="77d5c-123">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="77d5c-124">**IVdsSubSystemIscsi::QueryTargets**</span><span class="sxs-lookup"><span data-stu-id="77d5c-124">**IVdsSubSystemIscsi::QueryTargets**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets)
</dt> </dl>

 

 
