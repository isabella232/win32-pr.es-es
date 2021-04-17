---
description: Usar el CRM de COM+ en un entorno de clústeres
ms.assetid: 753461c5-880c-4df0-b552-b962dc06524f
title: Usar el CRM de COM+ en un entorno de clústeres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a05ff281748c35128349ef5d0d0f43d7beae86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360047"
---
# <a name="using-the-com-crm-in-a-cluster-environment"></a><span data-ttu-id="8fbd0-103">Usar el CRM de COM+ en un entorno de clústeres</span><span class="sxs-lookup"><span data-stu-id="8fbd0-103">Using the COM+ CRM in a Cluster Environment</span></span>

<span data-ttu-id="8fbd0-104">Al desarrollar CRMs de COM+ para trabajar en entornos de clústeres, el factor principal a tener en cuenta es si un CRM específico es el nodo del clúster en el que está trabajando.</span><span class="sxs-lookup"><span data-stu-id="8fbd0-104">When developing COM+ CRMs to work in cluster environments, the main factor to consider is whether a specific CRM cares which node of the cluster it is operating on.</span></span> <span data-ttu-id="8fbd0-105">Por ejemplo, si el recurso administrado por CRM es el sistema de archivos del equipo o el registro, los cambios son específicos del nodo en el que se ejecuta la aplicación de servidor CRM.</span><span class="sxs-lookup"><span data-stu-id="8fbd0-105">For example, if the resource managed by the CRM is the machine file system or registry, any changes are specific to the node that the CRM server application is running on at the time.</span></span> <span data-ttu-id="8fbd0-106">En este caso, no sería conveniente realizar la conmutación por error de la aplicación de servidor CRM a otro nodo.</span><span class="sxs-lookup"><span data-stu-id="8fbd0-106">In this case, failover of the CRM server application to another node would not be desirable.</span></span> <span data-ttu-id="8fbd0-107">En un caso diferente, en el que el CRM administra algún recurso común al clúster, es útil la conmutación por error de la aplicación de servidor CRM a otro nodo.</span><span class="sxs-lookup"><span data-stu-id="8fbd0-107">In a different case, where the CRM is managing some resource common to the cluster, failover of the CRM server application to another node is useful.</span></span>

<span data-ttu-id="8fbd0-108">La ubicación predeterminada del directorio para los archivos de registro de CRM es el mismo directorio que el archivo de registro de DTC.</span><span class="sxs-lookup"><span data-stu-id="8fbd0-108">The default directory location for CRM log files is the same directory as the DTC log file.</span></span> <span data-ttu-id="8fbd0-109">En los clústeres, el archivo de registro de DTC se coloca en un disco compartido que se conmuta por error entre los nodos del clúster.</span><span class="sxs-lookup"><span data-stu-id="8fbd0-109">On clusters, the DTC log file is placed on a shared disk that is failed over between the nodes of the cluster.</span></span> <span data-ttu-id="8fbd0-110">Esto significa que el comportamiento predeterminado de las aplicaciones de servidor CRM es la conmutación por error entre los nodos del clúster.</span><span class="sxs-lookup"><span data-stu-id="8fbd0-110">This means that the default behavior for CRM server applications is to failover between nodes of the cluster.</span></span> <span data-ttu-id="8fbd0-111">Por lo tanto, si un CRM específico requiere el comportamiento alternativo de no realizar una conmutación por error entre los nodos, se debe cambiar la ubicación del archivo de registro de CRM para esa aplicación de servidor CRM concreta.</span><span class="sxs-lookup"><span data-stu-id="8fbd0-111">Therefore, if a specific CRM requires the alternative behavior of not failing over between nodes, the location of the CRM log file for that particular CRM server application should be changed.</span></span>

<span data-ttu-id="8fbd0-112">Además, si se requiere la conmutación por error para la aplicación CRM, debe configurarse como una aplicación genérica en un grupo de clústeres.</span><span class="sxs-lookup"><span data-stu-id="8fbd0-112">In addition, if failover is required for the CRM application, it should be configured as a generic application in a cluster group.</span></span> <span data-ttu-id="8fbd0-113">Su dependencia debe ser DTC.</span><span class="sxs-lookup"><span data-stu-id="8fbd0-113">Its dependency should be DTC.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fbd0-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8fbd0-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fbd0-115">Conceptos de Administrador de recursos de compensación de COM+</span><span class="sxs-lookup"><span data-stu-id="8fbd0-115">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



