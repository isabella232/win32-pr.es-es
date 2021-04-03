---
description: Al conectarse de forma remota a un servidor de Active Directory que no sea el del dominio actual, debe especificar el nombre de un equipo que ya sea miembro del dominio que pertenece al Active Directory desea.
ms.assetid: f1478b9d-4a92-4340-8721-1f443eb6ace2
ms.tgt_platform: multiple
title: Descripción del espacio de nombres LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1f27c3e2ebc48a0dfa14563822e34bc06d6223
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083136"
---
# <a name="describing-the-ldap-namespace"></a><span data-ttu-id="e5dfe-103">Descripción del espacio de nombres LDAP</span><span class="sxs-lookup"><span data-stu-id="e5dfe-103">Describing the LDAP Namespace</span></span>

<span data-ttu-id="e5dfe-104">Al conectarse de forma remota a un servidor de Active Directory que no sea el del dominio actual, debe especificar el nombre de un equipo que ya sea miembro del dominio que pertenece al Active Directory desea.</span><span class="sxs-lookup"><span data-stu-id="e5dfe-104">When connecting remotely to an Active Directory server other than the one in your current domain, you must specify the name of a computer that is already a member of the domain belonging to the Active Directory you want.</span></span>

<span data-ttu-id="e5dfe-105">Para conectarse de forma remota a un equipo que ya es miembro del dominio que pertenece al servidor de Active Directory, escriba el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="e5dfe-105">To remotely connect to a computer that is already a member of the domain belonging to the Active Directory server, type the following command.</span></span>

<span data-ttu-id="e5dfe-106">**\\\\\\Directorio raíz de equiporemoto \\ \\ LDAP**</span><span class="sxs-lookup"><span data-stu-id="e5dfe-106">**\\\\RemoteComputer\\root\\directory\\LDAP**</span></span>

<span data-ttu-id="e5dfe-107">Este ejemplo muestra que hay dos partes que componen un nombre de espacio de nombres completo.</span><span class="sxs-lookup"><span data-stu-id="e5dfe-107">This example shows that there are two parts that make up a fully qualified namespace name.</span></span> <span data-ttu-id="e5dfe-108">La primera parte ( \\ \\ equiporemoto) representa el equipo que ya es miembro del dominio que pertenece al servidor Active Directory que desea.</span><span class="sxs-lookup"><span data-stu-id="e5dfe-108">The first part (\\\\RemoteComputer) represents the computer that is already a member of the domain belonging to the Active Directory server you want.</span></span> <span data-ttu-id="e5dfe-109">La segunda parte ( \\ \\ LDAP del directorio raíz \\ ) representa el esquema de Active Directory en el proveedor de servicios de directorio.</span><span class="sxs-lookup"><span data-stu-id="e5dfe-109">The second part (\\root\\directory\\LDAP) represents the Active Directory schema in the Directory Services Provider.</span></span>

> [!Note]  
> <span data-ttu-id="e5dfe-110">Para obtener más información acerca de la compatibilidad y la instalación de este componente en un sistema operativo específico, consulte [disponibilidad del sistema operativo de los componentes de WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="e5dfe-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



