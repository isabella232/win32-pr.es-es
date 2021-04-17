---
description: .
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: Eliminación de servicios UDDI del sistema operativo del servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7681167177b850ba44ac0fc26e019c7393008b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653011"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a><span data-ttu-id="cd772-103">Eliminación de servicios UDDI del sistema operativo del servidor</span><span class="sxs-lookup"><span data-stu-id="cd772-103">Removal of UDDI Services from Server Operating System</span></span>

## <a name="affected-platform"></a><span data-ttu-id="cd772-104">Plataforma afectada</span><span class="sxs-lookup"><span data-stu-id="cd772-104">Affected Platform</span></span>

<span data-ttu-id="cd772-105">**Servidores** : Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cd772-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="cd772-106">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="cd772-106">Feature Impact</span></span>

<span data-ttu-id="cd772-107">**Gravedad** : medio</span><span class="sxs-lookup"><span data-stu-id="cd772-107">**Severity** - Medium</span></span>  
<span data-ttu-id="cd772-108">**Frecuencia** : baja</span><span class="sxs-lookup"><span data-stu-id="cd772-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="cd772-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd772-109">Description</span></span>

<span data-ttu-id="cd772-110">Microsoft ha quitado la función de servidor de servicios UDDI (Universal Description, Discovery, and Integration) de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="cd772-110">Microsoft has removed the UDDI (Universal Description, Discovery, and Integration) Services server role from Windows Server 2008 R2.</span></span> <span data-ttu-id="cd772-111">Las versiones futuras de los servicios UDDI formarán parte del producto de Microsoft BizTalk.</span><span class="sxs-lookup"><span data-stu-id="cd772-111">Future releases of UDDI Services will be part of the Microsoft BizTalk product.</span></span> <span data-ttu-id="cd772-112">Esta realineación del producto y la consolidación sitúa a Microsoft para ofrecer un mejor servicio al mercado de la arquitectura orientada a servicios (SOA).</span><span class="sxs-lookup"><span data-stu-id="cd772-112">This product realignment and consolidation positions Microsoft to better serve the services-oriented architecture (SOA) market.</span></span>

<span data-ttu-id="cd772-113">La primera versión posterior a Windows Server 2008 de servicios UDDI será compatible con los estándares de UDDI v 3.0.</span><span class="sxs-lookup"><span data-stu-id="cd772-113">The first post-Windows Server 2008 release of UDDI Services will be UDDI v3.0 standards compliant.</span></span> <span data-ttu-id="cd772-114">Se incluirá como parte de la versión BizTalk Server 2009.</span><span class="sxs-lookup"><span data-stu-id="cd772-114">It will ship as part of the BizTalk Server 2009 release.</span></span> <span data-ttu-id="cd772-115">Para cumplir nuestro compromiso de proporcionar una experiencia de usuario satisfactoria, ofreceremos un paquete de instalación de servicios UDDI v3 para Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="cd772-115">To meet our commitment to provide a satisfactory user experience, we will offer a UDDI Services v3 installation package for Windows Server 2008 R2.</span></span>

## <a name="manifestation"></a><span data-ttu-id="cd772-116">Manifestación</span><span class="sxs-lookup"><span data-stu-id="cd772-116">Manifestation</span></span>

<span data-ttu-id="cd772-117">La presencia de versiones anteriores de los componentes de servicios UDDI en el sistema bloquea una actualización a Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="cd772-117">The presence of previous versions of UDDI Services components on the system blocks an upgrade to Windows Server 2008 R2.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="cd772-118">Mitigación del impacto</span><span class="sxs-lookup"><span data-stu-id="cd772-118">Mitigation of Impact</span></span>

<span data-ttu-id="cd772-119">Los usuarios que han implementado un sitio de servicios UDDI desde Windows Server 2003 o Windows Server 2008 pueden optar por no actualizar los servidores que ejecutan los servicios UDDI a Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="cd772-119">Users who have deployed a UDDI Services site from Windows Server 2003 or Windows Server 2008 can choose not to upgrade the servers running the UDDI Services to Windows Server 2008 R2.</span></span> <span data-ttu-id="cd772-120">También pueden trasladar los servicios UDDI a cuadros Windows Server 2003 o Windows Server 2008 dedicados si tienen que actualizar los cuadros de servicios UDDI actuales.</span><span class="sxs-lookup"><span data-stu-id="cd772-120">They can also move the UDDI Services to dedicated Windows Server 2003 or Windows Server 2008 boxes if they have to upgrade the current UDDI Services boxes.</span></span>

## <a name="solution"></a><span data-ttu-id="cd772-121">Solución</span><span class="sxs-lookup"><span data-stu-id="cd772-121">Solution</span></span>

<span data-ttu-id="cd772-122">La solución recomendada es implementar los servicios UDDI v 3.0 desde BizTalk Server 2009 en un equipo con Windows Server 2008 R2 y, a continuación, migrar el sitio anterior al nuevo sitio.</span><span class="sxs-lookup"><span data-stu-id="cd772-122">The recommended solution is to deploy UDDI Services v3.0 from BizTalk Server 2009 onto a Windows Server 2008 R2 machine, and then to migrate the old site to the new site.</span></span> <span data-ttu-id="cd772-123">Servicios UDDI v 3.0 proporciona compatibilidad con versiones anteriores de los servicios UDDI 2,0, por lo que las aplicaciones que usen servicios UDDI no se verán afectadas.</span><span class="sxs-lookup"><span data-stu-id="cd772-123">UDDI Services v3.0 provides backward compatibility with UDDI Services 2.0, so any applications that are using UDDI Services will be unaffected.</span></span>

<span data-ttu-id="cd772-124">Para ello, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="cd772-124">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="cd772-125">Configure un nuevo sitio de servicios UDDI 3.0 en un equipo ya cargado con Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="cd772-125">Set up a new UDDI Services v3.0 site on a machine already loaded with Windows Server 2008 R2.</span></span> <span data-ttu-id="cd772-126">(Nota: en una instalación distribuida, un sitio UDDI v 3.0 puede constar de más de una máquina con Windows Server 2008 R2).</span><span class="sxs-lookup"><span data-stu-id="cd772-126">(Note: In a distributed setup, a UDDI v3.0 site can consist of more than one Windows Server 2008 R2 machines.)</span></span>
2.  <span data-ttu-id="cd772-127">Use la herramienta de migración de datos UDDI para migrar los datos de la antigua base de datos de servicios UDDI a la nueva base de datos.</span><span class="sxs-lookup"><span data-stu-id="cd772-127">Use the UDDI data migration tool to migrate the data from the old UDDI Services database to the new database.</span></span>
3.  <span data-ttu-id="cd772-128">Realice una copia de seguridad de la antigua base de datos de servicios UDDI para garantizar la capacidad de reversión.</span><span class="sxs-lookup"><span data-stu-id="cd772-128">Back up the old UDDI Services database to ensure rollback capability.</span></span>
4.  <span data-ttu-id="cd772-129">Desinstale el antiguo software de servicios UDDI y, a continuación, actualice esas casillas a Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="cd772-129">Uninstall the old UDDI Services software and then upgrade those boxes to Windows Server 2008 R2.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="cd772-130">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="cd772-130">Links to Other Resources</span></span>

-   [<span data-ttu-id="cd772-131">Sitio web de servicios UDDI de Microsoft</span><span class="sxs-lookup"><span data-stu-id="cd772-131">Microsoft UDDI Services website</span></span>](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [<span data-ttu-id="cd772-132">Especificaciones de UDDI</span><span class="sxs-lookup"><span data-stu-id="cd772-132">UDDI specifications</span></span>](http://uddi.xml.org/specification)
-   [<span data-ttu-id="cd772-133">Descarga de servicios UDDI v 3.0 para Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cd772-133">UDDI Services v3.0 download for Windows Server 2008 R2</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



