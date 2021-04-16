---
description: El espacio de nombres LDAP (Protocolo ligero de acceso a directorios) y las rutas de acceso de la interfaz de Active Directory Services (ADSI) se suministran al llamar al proveedor de Active Directory a través de WMI.
ms.assetid: 55733fba-2170-4400-a516-896f6bf9525a
ms.tgt_platform: multiple
title: Usar la sintaxis de Active Directory adecuada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e321d6919c48103be930226cf11c4b3e82dcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706027"
---
# <a name="using-the-proper-active-directory-syntax"></a><span data-ttu-id="2d01a-103">Usar la sintaxis de Active Directory adecuada</span><span class="sxs-lookup"><span data-stu-id="2d01a-103">Using the Proper Active Directory Syntax</span></span>

<span data-ttu-id="2d01a-104">El espacio de nombres LDAP (Protocolo ligero de acceso a directorios) y las rutas de acceso de la interfaz de Active Directory Services (ADSI) se suministran al llamar al [proveedor de Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider) a través de WMI.</span><span class="sxs-lookup"><span data-stu-id="2d01a-104">You supply the Lightweight Directory Access Protocol (LDAP) namespace and Active Directory Services Interface (ADSI) paths when calling the [Active Directory Provider](/previous-versions/windows/desktop/dsprov/active-directory-provider) through WMI.</span></span>

<span data-ttu-id="2d01a-105">En los temas siguientes se describe el espacio de nombres LDAP y la ruta de acceso ADSI:</span><span class="sxs-lookup"><span data-stu-id="2d01a-105">The following topics describe the LDAP namespace and the ADSI path:</span></span>

-   [<span data-ttu-id="2d01a-106">Descripción del espacio de nombres LDAP</span><span class="sxs-lookup"><span data-stu-id="2d01a-106">Describing the LDAP Namespace</span></span>](describing-the-ldap-namespace.md)

    <span data-ttu-id="2d01a-107">Una ruta de acceso de espacio de nombres describe la ubicación de un espacio de nombres remoto.</span><span class="sxs-lookup"><span data-stu-id="2d01a-107">A namespace path describes the location of a remote namespace.</span></span> <span data-ttu-id="2d01a-108">Use la ruta de acceso del espacio de nombres para conectarse de forma remota a un espacio de nombres de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2d01a-108">Use the namespace path to connect remotely to an Active Directory namespace.</span></span>

-   [<span data-ttu-id="2d01a-109">Descripción de la ruta de acceso ADSI</span><span class="sxs-lookup"><span data-stu-id="2d01a-109">Describing the ADSI Path</span></span>](describing-the-adsi-path.md)

    <span data-ttu-id="2d01a-110">La ruta de acceso ADSI describe la ubicación de un objeto mediante la API ADSI.</span><span class="sxs-lookup"><span data-stu-id="2d01a-110">The ADSI path describes the location of an object using the ADSI API.</span></span> <span data-ttu-id="2d01a-111">Use la ruta de acceso ADSI en los parámetros que el proveedor pasa a Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2d01a-111">Use the ADSI path in parameters that the provider passes onto Active Directory.</span></span>

> [!Note]  
> <span data-ttu-id="2d01a-112">Para obtener más información acerca de la compatibilidad y la instalación de este componente en un sistema operativo específico, consulte [disponibilidad del sistema operativo de los componentes de WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="2d01a-112">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 
