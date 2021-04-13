---
description: Como alternativa a la administración de particiones Active Directory a través de la herramienta administrativa usuarios y equipos Active Directory, puede administrar particiones COM+ mediante programación a través del uso de un conjunto de objetos COM+ en Active Directory interfaz del sistema (ADSI).
ms.assetid: 915b4643-cbda-433a-a383-65a6b0fd0874
title: Administrar particiones en Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6635e49b7d2833a1e6e177c25f9f2fb05ff0dff4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539285"
---
# <a name="managing-partitions-within-active-directory"></a><span data-ttu-id="ef99b-103">Administrar particiones en Active Directory</span><span class="sxs-lookup"><span data-stu-id="ef99b-103">Managing Partitions Within Active Directory</span></span>

<span data-ttu-id="ef99b-104">Como alternativa a la administración de particiones Active Directory a través de la herramienta administrativa usuarios y equipos Active Directory, puede administrar particiones COM+ mediante programación a través del uso de un conjunto de objetos COM+ en Active Directory interfaz del sistema (ADSI).</span><span class="sxs-lookup"><span data-stu-id="ef99b-104">As an alternative to managing Active Directory partitions through the Active Directory Users and Computers administrative tool, you can manage COM+ partitions programmatically through the use of a set of COM+ objects within Active Directory System Interface (ADSI).</span></span>

<span data-ttu-id="ef99b-105">Independientemente de la técnica administrativa que elija para administrar particiones COM+, hay una secuencia general de pasos que deben seguir los administradores:</span><span class="sxs-lookup"><span data-stu-id="ef99b-105">Regardless of the administrative technique you choose for managing COM+ partitions, there is a general sequence of steps that administrators must follow:</span></span>

1.  <span data-ttu-id="ef99b-106">Cree las nuevas particiones COM+ en Active Directory para el dominio.</span><span class="sxs-lookup"><span data-stu-id="ef99b-106">Create the new COM+ partitions within Active Directory for your domain.</span></span>
2.  <span data-ttu-id="ef99b-107">Crear conjuntos de particiones COM+ en Active Directory y asignarlos a las particiones COM+ recién creadas.</span><span class="sxs-lookup"><span data-stu-id="ef99b-107">Create COM+ partition sets within Active Directory, and map them to your newly created COM+ partitions.</span></span>
3.  <span data-ttu-id="ef99b-108">Configure las particiones de Active Directory en el equipo local con el objeto COM+ adecuado.</span><span class="sxs-lookup"><span data-stu-id="ef99b-108">Configure your Active Directory partitions on your local machine, using the appropriate COM+ object.</span></span> <span data-ttu-id="ef99b-109">Al configurar una partición de Active Directory en un equipo local, se crea automáticamente una carpeta de **aplicaciones com+** en esa carpeta de partición.</span><span class="sxs-lookup"><span data-stu-id="ef99b-109">When you configure an Active Directory partition on a local machine, a **COM+ Applications** folder is automatically created in that partition folder.</span></span>
4.  <span data-ttu-id="ef99b-110">Instale las aplicaciones COM+ en las particiones COM+ apropiadas.</span><span class="sxs-lookup"><span data-stu-id="ef99b-110">Install your COM+ applications in the appropriate COM+ partitions.</span></span>

<span data-ttu-id="ef99b-111">Todos los pasos anteriores se pueden realizar mediante programación, mediante un conjunto de interfaces de Active Directory denominadas ADSI.</span><span class="sxs-lookup"><span data-stu-id="ef99b-111">All of the preceding steps can be done programmatically, using a set of Active Directory interfaces called ADSI.</span></span> <span data-ttu-id="ef99b-112">Los objetos disponibles para administrar las particiones que están disponibles en ADSI son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="ef99b-112">The objects available for managing partitions that are available within ADSI are as follows:</span></span>

-   <span data-ttu-id="ef99b-113">\_nombre de USERPARTITIONSETLINK de DS \_</span><span class="sxs-lookup"><span data-stu-id="ef99b-113">DS\_USERPARTITIONSETLINK\_NAME</span></span>
-   <span data-ttu-id="ef99b-114">\_nombre de PARTITIONLINK de DS \_</span><span class="sxs-lookup"><span data-stu-id="ef99b-114">DS\_PARTITIONLINK\_NAME</span></span>
-   <span data-ttu-id="ef99b-115">nombre de DS \_ objectId \_</span><span class="sxs-lookup"><span data-stu-id="ef99b-115">DS\_OBJECTID\_NAME</span></span>
-   <span data-ttu-id="ef99b-116">\_nombre de DEFAULTPARTITIONLINK de DS \_</span><span class="sxs-lookup"><span data-stu-id="ef99b-116">DS\_DEFAULTPARTITIONLINK\_NAME</span></span>
-   <span data-ttu-id="ef99b-117">\_nombre de USERLINK de DS \_</span><span class="sxs-lookup"><span data-stu-id="ef99b-117">DS\_USERLINK\_NAME</span></span>
-   <span data-ttu-id="ef99b-118">\_nombre de PARTITIONSET de DS \_</span><span class="sxs-lookup"><span data-stu-id="ef99b-118">DS\_PARTITIONSET\_NAME</span></span>
-   <span data-ttu-id="ef99b-119">\_nombre de partición de DS \_</span><span class="sxs-lookup"><span data-stu-id="ef99b-119">DS\_PARTITION\_NAME</span></span>

<span data-ttu-id="ef99b-120">Para obtener información sobre cómo crear y administrar particiones COM+ mediante el uso de las herramientas administrativas Active Directory usuarios y equipos y servicios de componentes, vea la ayuda en pantalla disponible en cada herramienta.</span><span class="sxs-lookup"><span data-stu-id="ef99b-120">For information on creating and managing COM+ partitions through the use of the Active Directory Users and Computers and Component Services administrative tools, see the online help available from within each tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef99b-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ef99b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef99b-122">Recopilación de métricas de partición</span><span class="sxs-lookup"><span data-stu-id="ef99b-122">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="ef99b-123">Configuración de la memoria caché de partición</span><span class="sxs-lookup"><span data-stu-id="ef99b-123">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="ef99b-124">Agrupar aplicaciones en particiones</span><span class="sxs-lookup"><span data-stu-id="ef99b-124">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="ef99b-125">Administrar particiones locales</span><span class="sxs-lookup"><span data-stu-id="ef99b-125">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="ef99b-126">Establecer derechos administrativos para una partición</span><span class="sxs-lookup"><span data-stu-id="ef99b-126">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



