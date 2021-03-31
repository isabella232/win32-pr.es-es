---
description: Active Directory es el servicio de directorio para Windows y es la base de las redes distribuidas de Windows.
ms.assetid: e7569754-87c3-4a18-bfed-a03a32a2ee22
ms.tgt_platform: multiple
title: Obtener acceso a Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbad433f1f189d68c8a7ab2f312cbb678b15ee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278775"
---
# <a name="accessing-active-directory"></a><span data-ttu-id="adfa8-103">Obtener acceso a Active Directory</span><span class="sxs-lookup"><span data-stu-id="adfa8-103">Accessing Active Directory</span></span>

<span data-ttu-id="adfa8-104">Active Directory es el servicio de directorio para Windows y es la base de las redes distribuidas de Windows.</span><span class="sxs-lookup"><span data-stu-id="adfa8-104">Active Directory is the directory service for Windows and is the foundation of Windows distributed networks.</span></span> <span data-ttu-id="adfa8-105">Puede usar Active Directory para buscar objetos en un dominio de red del equipo, como usuarios, directivas de seguridad, impresoras, componentes distribuidos y otros recursos.</span><span class="sxs-lookup"><span data-stu-id="adfa8-105">You can use Active Directory to locate objects in a computer network domain, such as users, security policies, printers, distributed components, and other resources.</span></span> <span data-ttu-id="adfa8-106">El nombre Active Directory hace referencia al servicio de directorio y al propio directorio.</span><span class="sxs-lookup"><span data-stu-id="adfa8-106">The name Active Directory refers both to the directory service and the directory itself.</span></span>

> [!Note]  
> <span data-ttu-id="adfa8-107">Para obtener más información acerca de la compatibilidad y la instalación de este componente en un sistema operativo específico, consulte [disponibilidad del sistema operativo de los componentes de WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="adfa8-107">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

<span data-ttu-id="adfa8-108">Windows hace Active Directory accesible a través de WMI mediante la creación de un conjunto de referencias a cada clase y objeto incluidos en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="adfa8-108">Windows makes Active Directory accessible through WMI by creating a set of references to every class and object contained in Active Directory.</span></span> <span data-ttu-id="adfa8-109">Al tener acceso al proveedor de servicios de directorio a través de WMI, puede crear aplicaciones habilitadas para WMI que puedan tener acceso a la riqueza de la información contenida en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="adfa8-109">By accessing the Directory Services provider through WMI, you can create WMI-enabled applications that can access the wealth of information contained in Active Directory.</span></span>

<span data-ttu-id="adfa8-110">Con estas interfaces, puede:</span><span class="sxs-lookup"><span data-stu-id="adfa8-110">With these interfaces, you can:</span></span>

-   <span data-ttu-id="adfa8-111">Recuperar clases e instancias.</span><span class="sxs-lookup"><span data-stu-id="adfa8-111">Retrieve classes and instances.</span></span>
-   <span data-ttu-id="adfa8-112">Enumerar clases e instancias.</span><span class="sxs-lookup"><span data-stu-id="adfa8-112">Enumerate classes and instances.</span></span>
-   <span data-ttu-id="adfa8-113">Cree nuevas instancias.</span><span class="sxs-lookup"><span data-stu-id="adfa8-113">Create new instances.</span></span>
-   <span data-ttu-id="adfa8-114">Modifique las instancias existentes.</span><span class="sxs-lookup"><span data-stu-id="adfa8-114">Modify existing instances.</span></span>
-   <span data-ttu-id="adfa8-115">Elimine las instancias existentes.</span><span class="sxs-lookup"><span data-stu-id="adfa8-115">Delete existing instances.</span></span>
-   <span data-ttu-id="adfa8-116">Active Directory de consultas.</span><span class="sxs-lookup"><span data-stu-id="adfa8-116">Query Active Directory.</span></span>

<span data-ttu-id="adfa8-117">Los temas siguientes pueden ayudarle a usar Active Directory con WMI:</span><span class="sxs-lookup"><span data-stu-id="adfa8-117">The following topics can assist you in using Active Directory with WMI:</span></span>

-   [<span data-ttu-id="adfa8-118">Usar la sintaxis de Active Directory adecuada</span><span class="sxs-lookup"><span data-stu-id="adfa8-118">Using the Proper Active Directory Syntax</span></span>](using-the-proper-active-directory-syntax.md)
-   [<span data-ttu-id="adfa8-119">Asignación de Active Directory a WMI</span><span class="sxs-lookup"><span data-stu-id="adfa8-119">Mapping Active Directory to WMI</span></span>](mapping-active-directory-to-wmi.md)

 

 



