---
description: El proveedor de servicios de directorio refleja las clases e instancias de Active Directory en el espacio de nombres LDAP (Protocolo ligero de acceso a directorios) de WMI.
ms.assetid: 0215b614-cb10-4195-837d-bf81d523c560
ms.tgt_platform: multiple
title: Asignación de Active Directory a WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0162f722eb8a053270ac2a8e75eaed4f1cd405
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667869"
---
# <a name="mapping-active-directory-to-wmi"></a><span data-ttu-id="50d24-103">Asignación de Active Directory a WMI</span><span class="sxs-lookup"><span data-stu-id="50d24-103">Mapping Active Directory to WMI</span></span>

<span data-ttu-id="50d24-104">El proveedor de servicios de directorio refleja las clases e instancias de Active Directory en el espacio de nombres LDAP (Protocolo ligero de acceso a directorios) de WMI.</span><span class="sxs-lookup"><span data-stu-id="50d24-104">The Directory Services Provider mirrors classes and instances from Active Directory into the WMI Lightweight Directory Access Protocol (LDAP) namespace.</span></span> <span data-ttu-id="50d24-105">Debido a las diferencias fundamentales en los dos entornos, no puede simplemente cambiar el nombre de las clases e instancias de Active Directory y esperar tener acceso correctamente a esas clases e instancias en WMI.</span><span class="sxs-lookup"><span data-stu-id="50d24-105">Because of fundamental differences in the two environments, you cannot simply rename the Active Directory classes and instances and hope to properly access those classes and instances in WMI.</span></span> <span data-ttu-id="50d24-106">En su lugar, el proveedor de servicios de directorio sigue las reglas de nomenclatura para conservar las relaciones que existen entre las clases e instancias de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="50d24-106">Instead, the Directory Services provider follows naming rules to preserve the relationships that exist between the Active Directory classes and instances.</span></span>

<span data-ttu-id="50d24-107">En los temas siguientes se proporciona información acerca de la asignación de clases e instancias de Active Directory:</span><span class="sxs-lookup"><span data-stu-id="50d24-107">The following topics provide information about mapping Active Directory classes and instances:</span></span>

-   [<span data-ttu-id="50d24-108">Asignar Active Directory clases</span><span class="sxs-lookup"><span data-stu-id="50d24-108">Mapping Active Directory Classes</span></span>](mapping-active-directory-classes.md)
-   [<span data-ttu-id="50d24-109">Asignación de instancias de Active Directory</span><span class="sxs-lookup"><span data-stu-id="50d24-109">Mapping Active Directory Instances</span></span>](mapping-active-directory-instances.md)

> [!Note]  
> <span data-ttu-id="50d24-110">Para obtener más información acerca de la compatibilidad y la instalación de este componente en un sistema operativo específico, consulte [disponibilidad del sistema operativo de los componentes de WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="50d24-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



