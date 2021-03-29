---
title: Eliminar una partición de directorio de aplicaciones
description: Una partición de directorio de aplicaciones se elimina eliminando el objeto crossRef que representa la partición del directorio de aplicaciones.
ms.assetid: bc7986c1-5a11-440c-924e-dc525b5cb78f
ms.tgt_platform: multiple
keywords:
- Eliminar una partición de directorio de aplicaciones AD
- Particiones de directorio de aplicaciones, eliminar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd52ef99323ee7463a4733210314e02d911f0d66
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789580"
---
# <a name="deleting-an-application-directory-partition"></a><span data-ttu-id="b49b2-105">Eliminar una partición de directorio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="b49b2-105">Deleting an Application Directory Partition</span></span>

<span data-ttu-id="b49b2-106">Una partición de directorio de aplicaciones se elimina eliminando el objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa la partición del directorio de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b49b2-106">An application directory partition is deleted by deleting the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that represents the application directory partition.</span></span> <span data-ttu-id="b49b2-107">Cuando la eliminación del objeto **crossRef** se replica en un controlador de dominio que tiene una réplica de la partición de directorio de aplicaciones, el KCC eliminará la réplica local de la partición de directorio de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b49b2-107">When the deletion of the **crossRef** object replicates to a domain controller that has a replica of the application directory partition, the KCC will delete the local replica of the application directory partition.</span></span> <span data-ttu-id="b49b2-108">Esto hace que se eliminen todas las réplicas de la partición de directorio de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b49b2-108">This eventually causes all replicas of the application directory partition to be deleted.</span></span>

<span data-ttu-id="b49b2-109">Cuando se elimina el objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) , el servidor de Active Directory eliminará el objeto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) que se creó cuando se creó la partición del directorio de aplicaciones, así como la eliminación de todos los objetos de la partición del directorio de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b49b2-109">When the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object is deleted, the Active Directory server will delete the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object that was created when the application directory partition was created, as well as deleting all objects in the application directory partition.</span></span> <span data-ttu-id="b49b2-110">Ninguno de los objetos de la partición de directorio de aplicaciones se extingue cuando se eliminan.</span><span class="sxs-lookup"><span data-stu-id="b49b2-110">None of the objects in the application directory partition are tombstoned when they deleted.</span></span>

<span data-ttu-id="b49b2-111">Cuando se elimina una partición de directorio de aplicaciones, es muy difícil restaurarla.</span><span class="sxs-lookup"><span data-stu-id="b49b2-111">When an application directory partition is deleted, it is very difficult to restore it.</span></span> <span data-ttu-id="b49b2-112">Para restaurar una partición de directorio de aplicaciones, es necesario restaurar una copia de seguridad que tenga una réplica de la partición de directorio de aplicaciones, buscar el objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa la partición del directorio de aplicaciones y restaurar de forma autoritativa el objeto **crossRef** .</span><span class="sxs-lookup"><span data-stu-id="b49b2-112">To restore an application directory partition, it is necessary to restore a backup that has a replica of the application directory partition, find the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that represents the application directory partition and authoritatively restore the **crossRef** object.</span></span>

<span data-ttu-id="b49b2-113">**Para eliminar una partición del directorio de aplicaciones y sus réplicas, realice los pasos siguientes:**</span><span class="sxs-lookup"><span data-stu-id="b49b2-113">**To delete an application directory partition and its replicas, perform the following steps**</span></span>

1.  <span data-ttu-id="b49b2-114">Busque en el contenedor de particiones un objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que tenga un valor de atributo [**NCName**](/windows/desktop/ADSchema/a-ncname) que sea igual al nombre distintivo de la partición de directorio de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b49b2-114">Search the Partitions container for a [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that has an [**nCName**](/windows/desktop/ADSchema/a-ncname) attribute value that is equal to the distinguished name of the application directory partition.</span></span>
2.  <span data-ttu-id="b49b2-115">Elimine el objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) .</span><span class="sxs-lookup"><span data-stu-id="b49b2-115">Delete the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object.</span></span>

<span data-ttu-id="b49b2-116">Para obtener más información, consulte el [código de ejemplo para eliminar una partición de directorio de aplicaciones](example-code-for-deleting-an-application-directory-partition.md).</span><span class="sxs-lookup"><span data-stu-id="b49b2-116">For more information, see [Example Code for Deleting an Application Directory Partition](example-code-for-deleting-an-application-directory-partition.md).</span></span>

 

 