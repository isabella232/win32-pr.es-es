---
description: Establecer derechos administrativos para una partición
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: Establecer derechos administrativos para una partición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c421b37dd50fa21ee9cf146749ec00b0c91d98c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807358"
---
# <a name="setting-administrative-rights-for-a-partition"></a><span data-ttu-id="3880b-103">Establecer derechos administrativos para una partición</span><span class="sxs-lookup"><span data-stu-id="3880b-103">Setting Administrative Rights for a Partition</span></span>

<span data-ttu-id="3880b-104">Los usuarios a los que se ha asignado el rol de administrador de la aplicación del sistema COM+ pueden crear, modificar y eliminar particiones de COM+.</span><span class="sxs-lookup"><span data-stu-id="3880b-104">Users assigned the Administrator role of the COM+ System Application are allowed to create, modify, and delete COM+ partitions.</span></span> <span data-ttu-id="3880b-105">En la herramienta administrativa Servicios de componentes, los roles administrativos se pueden asignar a los usuarios expandiendo la carpeta **roles** de la aplicación del sistema com+.</span><span class="sxs-lookup"><span data-stu-id="3880b-105">Within the Component Services administrative tool, administrative roles can be assigned to users by expanding the **Roles** folder of the COM+ System Application.</span></span>

<span data-ttu-id="3880b-106">A partir de Windows Server 2003, la capacidad de autenticación para la aplicación del sistema COM+ incluye el valor EOAC \_ Disable \_ AAA.</span><span class="sxs-lookup"><span data-stu-id="3880b-106">As of Windows Server 2003, the authentication capability for the COM+ System Application includes the value EOAC\_DISABLE\_AAA.</span></span> <span data-ttu-id="3880b-107">Este valor, que deshabilita las activaciones de activación como activador (AAA), se utiliza en la llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) al iniciar la aplicación del sistema.</span><span class="sxs-lookup"><span data-stu-id="3880b-107">This value, which disables activate-as-activator (AAA) activations, is used in the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) call when launching the System Application.</span></span> <span data-ttu-id="3880b-108">Establecer la capacidad de autenticación en EOAC \_ deshabilitar \_ AAA permite que una aplicación que se ejecuta en una cuenta con privilegios (como LocalSystem) ayude a evitar que se use su identidad para iniciar componentes que no son de confianza.</span><span class="sxs-lookup"><span data-stu-id="3880b-108">Setting the authentication capability to EOAC\_DISABLE\_AAA allows an application that runs under a privileged account (such as LocalSystem) to help prevent its identity from being used to launch untrusted components.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3880b-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3880b-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3880b-110">Recopilación de métricas de partición</span><span class="sxs-lookup"><span data-stu-id="3880b-110">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="3880b-111">Configuración de la memoria caché de partición</span><span class="sxs-lookup"><span data-stu-id="3880b-111">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="3880b-112">Agrupar aplicaciones en particiones</span><span class="sxs-lookup"><span data-stu-id="3880b-112">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="3880b-113">Administrar particiones locales</span><span class="sxs-lookup"><span data-stu-id="3880b-113">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="3880b-114">Administrar particiones en Active Directory</span><span class="sxs-lookup"><span data-stu-id="3880b-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> </dl>

 

 
