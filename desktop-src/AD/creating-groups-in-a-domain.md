---
title: Crear grupos en un dominio
description: Se crea un objeto de grupo en Active Directory Domain Services en el contenedor de dominio donde se incluirá el nuevo grupo.
ms.assetid: 40792878-4219-4242-8cf7-b092b28f2ff4
ms.tgt_platform: multiple
keywords:
- agrupa AD, crear grupos en un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100700b08fb82b750ee68dfed6bcb26060929e87
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077542"
---
# <a name="creating-groups-in-a-domain"></a><span data-ttu-id="f47df-104">Crear grupos en un dominio</span><span class="sxs-lookup"><span data-stu-id="f47df-104">Creating Groups in a Domain</span></span>

<span data-ttu-id="f47df-105">Se crea un objeto de grupo en Active Directory Domain Services en el contenedor de dominio donde se incluirá el nuevo grupo.</span><span class="sxs-lookup"><span data-stu-id="f47df-105">A group object is created in Active Directory Domain Services in the domain container where the new group will be contained.</span></span> <span data-ttu-id="f47df-106">Los grupos se pueden crear en la raíz del dominio, dentro de una unidad organizativa o dentro de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="f47df-106">Groups can be created at the root of the domain, within an organizational unit, or within a container.</span></span> <span data-ttu-id="f47df-107">Para crear un objeto de grupo, use el método [**IADsContainer:: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) o [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .</span><span class="sxs-lookup"><span data-stu-id="f47df-107">To create a group object, use the [**IADsContainer::Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) or the [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) method.</span></span>

<span data-ttu-id="f47df-108">Los atributos siguientes son necesarios para convertir el objeto de grupo en un grupo legal que reconozcan el servidor de Active Directory y el sistema de seguridad de Windows:</span><span class="sxs-lookup"><span data-stu-id="f47df-108">The following attributes are required to make the group object a legal group that the Active Directory server and the Windows security system will recognize:</span></span>

<dl> <dt>

<span data-ttu-id="f47df-109"><span id="cn"></span><span id="CN"></span>**CN**</span><span class="sxs-lookup"><span data-stu-id="f47df-109"><span id="cn"></span><span id="CN"></span>**cn**</span></span>
</dt> <dd>

<span data-ttu-id="f47df-110">Especifica el nombre del objeto de grupo en el directorio.</span><span class="sxs-lookup"><span data-stu-id="f47df-110">Specifies the name of the group object in the directory.</span></span> <span data-ttu-id="f47df-111">Este será el nombre distintivo relativo del objeto dentro del contenedor donde se crea el grupo.</span><span class="sxs-lookup"><span data-stu-id="f47df-111">This will be the object's relative distinguished name within the container where the group is created.</span></span>

</dd> <dt>

<span data-ttu-id="f47df-112"><span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**</span><span class="sxs-lookup"><span data-stu-id="f47df-112"><span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**</span></span>
</dt> <dd>

<span data-ttu-id="f47df-113">Contiene un entero que especifica el tipo y el ámbito de grupo.</span><span class="sxs-lookup"><span data-stu-id="f47df-113">Contains an integer that specifies the group type and scope.</span></span> <span data-ttu-id="f47df-114">La enumeración de enumeración de [**\_ \_ tipo \_ de grupo ADS**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) define los valores posibles para el atributo **GroupType** .</span><span class="sxs-lookup"><span data-stu-id="f47df-114">The [**ADS\_GROUP\_TYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) enumeration defines the possible values for the **groupType** attribute.</span></span>

<span data-ttu-id="f47df-115">En la lista siguiente se definen los tipos y valores de grupo comunes para este atributo.</span><span class="sxs-lookup"><span data-stu-id="f47df-115">The following list defines common group types and values for this attribute.</span></span>

<dl> <dt>

<span data-ttu-id="f47df-116"><span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Distribución local de dominio</span><span class="sxs-lookup"><span data-stu-id="f47df-116"><span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Domain Local Distribution</span></span>
</dt> <dd>

<span data-ttu-id="f47df-117">**tipo de grupo de ADS \_ \_ \_ \_ grupo local de dominio \_**</span><span class="sxs-lookup"><span data-stu-id="f47df-117">**ADS\_GROUP\_TYPE\_DOMAIN\_LOCAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="f47df-118"><span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Seguridad local de dominio</span><span class="sxs-lookup"><span data-stu-id="f47df-118"><span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Domain Local Security</span></span>
</dt> <dd>

<span data-ttu-id="f47df-119">**Anuncios \_ de tipo de grupo de grupo \_ \_ local de dominio \_ \_** \| **ADS seguridad de grupo \_ \_ \_ \_ habilitada**</span><span class="sxs-lookup"><span data-stu-id="f47df-119">**ADS\_GROUP\_TYPE\_DOMAIN\_LOCAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>

<span data-ttu-id="f47df-120"><span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Distribución global</span><span class="sxs-lookup"><span data-stu-id="f47df-120"><span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Global Distribution</span></span>
</dt> <dd>

<span data-ttu-id="f47df-121">**\_ \_ grupo global de tipo de grupo de \_ ADS \_**</span><span class="sxs-lookup"><span data-stu-id="f47df-121">**ADS\_GROUP\_TYPE\_GLOBAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="f47df-122"><span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Seguridad global</span><span class="sxs-lookup"><span data-stu-id="f47df-122"><span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Global Security</span></span>
</dt> <dd>

<span data-ttu-id="f47df-123">**Anuncios \_ de tipo de grupo de grupo de ADS de \_ \_ \_ grupo global** \| **\_ \_ \_ \_ habilitado para seguridad**</span><span class="sxs-lookup"><span data-stu-id="f47df-123">**ADS\_GROUP\_TYPE\_GLOBAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>

<span data-ttu-id="f47df-124"><span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Distribución universal</span><span class="sxs-lookup"><span data-stu-id="f47df-124"><span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Universal Distribution</span></span>
</dt> <dd>

<span data-ttu-id="f47df-125">**tipo de grupo de ADS \_ \_ \_ \_ grupo universal**</span><span class="sxs-lookup"><span data-stu-id="f47df-125">**ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="f47df-126"><span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Seguridad universal</span><span class="sxs-lookup"><span data-stu-id="f47df-126"><span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Universal Security</span></span>
</dt> <dd>

<span data-ttu-id="f47df-127">**Anuncios \_ de tipo de grupo de grupo de ADS de \_ \_ \_ grupo universal** \| **\_ \_ \_ \_ habilitado para seguridad**</span><span class="sxs-lookup"><span data-stu-id="f47df-127">**ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>


</dt> <dd>

</dd> </dl>

<span data-ttu-id="f47df-128">Si el grupo está pensado para establecer el control de acceso en los objetos de directorio, el grupo debe ser un grupo de seguridad global o de seguridad universal.</span><span class="sxs-lookup"><span data-stu-id="f47df-128">If the group is intended for setting access control on directory objects, the group should be a Global Security or Universal Security group.</span></span>

<span data-ttu-id="f47df-129">Tenga en cuenta que los grupos de seguridad universal solo se pueden crear en los dominios de Windows 2000 que se ejecutan en modo nativo.</span><span class="sxs-lookup"><span data-stu-id="f47df-129">Be aware that Universal Security groups can only be created on Windows 2000 domains running in native mode.</span></span> <span data-ttu-id="f47df-130">Para obtener más información acerca de cómo detectar el modo mixto y nativo, consulte [detectar el modo de operación de un dominio](detecting-the-operation-mode-of-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="f47df-130">For more information about detecting mixed and native mode, see [Detecting the Operation Mode of a Domain](detecting-the-operation-mode-of-a-domain.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47df-131"><span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f47df-131"><span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**</span></span>
</dt> <dd>

<span data-ttu-id="f47df-132">Contiene una cadena que es el nombre que se usa para admitir clientes y servidores de una versión anterior.</span><span class="sxs-lookup"><span data-stu-id="f47df-132">Contains a string that is the name used to support clients and servers from a previous version.</span></span> <span data-ttu-id="f47df-133">**SamAccountName** debe tener menos de 20 caracteres para admitir clientes de una versión anterior de Windows.</span><span class="sxs-lookup"><span data-stu-id="f47df-133">The **sAMAccountName** should be less than 20 characters to support clients of a previous version of Windows.</span></span>

<span data-ttu-id="f47df-134">**SamAccountName** debe ser único entre todos los objetos de entidad de seguridad del dominio.</span><span class="sxs-lookup"><span data-stu-id="f47df-134">The **sAMAccountName** must be unique among all security principal objects within the domain.</span></span> <span data-ttu-id="f47df-135">Se debe realizar una consulta en el dominio para comprobar que **samAccountName** es único en el dominio.</span><span class="sxs-lookup"><span data-stu-id="f47df-135">A query should be performed against the domain to verify that the **sAMAccountName** is unique within the domain.</span></span>

</dd> </dl>

<span data-ttu-id="f47df-136">Los miembros del grupo se pueden agregar en el momento de la creación mediante el método [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .</span><span class="sxs-lookup"><span data-stu-id="f47df-136">The members of the group can be added at creation time using the [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) method.</span></span> <span data-ttu-id="f47df-137">Opcionalmente, los miembros se pueden agregar al grupo después de la creación mediante el método [**IADsGroup:: Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) .</span><span class="sxs-lookup"><span data-stu-id="f47df-137">Optionally, members can be added to the group after creation using the [**IADsGroup::Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) method.</span></span> <span data-ttu-id="f47df-138">Para obtener más información sobre cómo agregar miembros a un grupo, consulte [Agregar miembros a grupos en un dominio](adding-members-to-groups-in-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="f47df-138">For more information about adding members to a group, see [Adding Members to Groups in a Domain](adding-members-to-groups-in-a-domain.md).</span></span>

 

 