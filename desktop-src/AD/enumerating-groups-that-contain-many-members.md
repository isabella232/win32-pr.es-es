---
title: Enumerar grupos que contienen muchos miembros
description: Los miembros de un grupo se almacenan en un atributo de varios valores denominado Member.
ms.assetid: 78f81b09-2223-4b74-b8d5-7a97494c0324
ms.tgt_platform: multiple
keywords:
- Enumerar grupos que contienen muchos miembros Active Directory
- grupos Active Directory, enumerar grupos con muchos miembros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2d9a5c9abc6e77ac72672379789d1028f92c3f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149180"
---
# <a name="enumerating-groups-that-contain-many-members"></a><span data-ttu-id="8f85d-105">Enumerar grupos que contienen muchos miembros</span><span class="sxs-lookup"><span data-stu-id="8f85d-105">Enumerating Groups That Contain Many Members</span></span>

<span data-ttu-id="8f85d-106">Los miembros de un grupo se almacenan en un atributo de varios valores denominado **member**.</span><span class="sxs-lookup"><span data-stu-id="8f85d-106">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="8f85d-107">El atributo de **miembro** puede contener un gran número de valores.</span><span class="sxs-lookup"><span data-stu-id="8f85d-107">The **member** attribute can contain a large number of values.</span></span> <span data-ttu-id="8f85d-108">La enumeración de miembros puede ser ineficaz cuando el número de valores de un atributo con varios valores llega a ser grande.</span><span class="sxs-lookup"><span data-stu-id="8f85d-108">Enumerating members can be inefficient when the number of values in a multi-valued attribute becomes large.</span></span> <span data-ttu-id="8f85d-109">El servidor también limitará el número máximo de valores que se pueden recuperar en una sola consulta.</span><span class="sxs-lookup"><span data-stu-id="8f85d-109">The server will also limit the maximum number of values that can be retrieved in a single query.</span></span> <span data-ttu-id="8f85d-110">Esto significa que si un grupo puede tener más miembros de los que puede proporcionar el servidor, la única manera de enumerar todos los miembros es usar la recuperación incremental de los datos, lo que se conoce como *recuperación de intervalo*.</span><span class="sxs-lookup"><span data-stu-id="8f85d-110">This means that if a group may have more members than can be supplied by the server, the only way to enumerate all members is to use incremental retrieval of data, known as *range retrieval*.</span></span>

<span data-ttu-id="8f85d-111">La recuperación por rangos implica solicitar un número limitado de valores de atributo en una sola consulta.</span><span class="sxs-lookup"><span data-stu-id="8f85d-111">Range retrieval involves requesting a limited number of attribute values in a single query.</span></span> <span data-ttu-id="8f85d-112">El número de valores solicitados debe ser menor o igual que el número máximo de valores admitidos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="8f85d-112">The number of values requested must be less than, or equal to, the maximum number of values supported by the server.</span></span> <span data-ttu-id="8f85d-113">Para reducir el número de veces que la consulta debe ponerse en contacto con el servidor, el número de valores solicitados debe ser lo más cercano posible a este máximo.</span><span class="sxs-lookup"><span data-stu-id="8f85d-113">To reduce the number of times the query must contact the server, the number of values requested should be as close, as possible, to this maximum.</span></span> <span data-ttu-id="8f85d-114">Para permitir que una aplicación funcione correctamente con todos los servidores, debe usarse un número máximo de 1000.</span><span class="sxs-lookup"><span data-stu-id="8f85d-114">To enable an application to work correctly with all servers, a maximum number of 1000 should be used.</span></span>

<span data-ttu-id="8f85d-115">La versión del servidor que proporciona los datos solicitados determina el número máximo de valores que se pueden recuperar en una sola consulta.</span><span class="sxs-lookup"><span data-stu-id="8f85d-115">The version of the server that supplies the requested data determines the maximum number of values that can be retrieved in a single query.</span></span> <span data-ttu-id="8f85d-116">En la tabla siguiente se muestra la versión del servidor y el número máximo de valores que se pueden recuperar en una sola consulta.</span><span class="sxs-lookup"><span data-stu-id="8f85d-116">The following table lists the server version and the maximum number of values that can be retrieved in a single query.</span></span>



| <span data-ttu-id="8f85d-117">Versión del sistema operativo del servidor</span><span class="sxs-lookup"><span data-stu-id="8f85d-117">Server operating system version</span></span> | <span data-ttu-id="8f85d-118">Máximo de valores recuperados</span><span class="sxs-lookup"><span data-stu-id="8f85d-118">Maximum values retrieved</span></span> |
|---------------------------------|--------------------------|
| <span data-ttu-id="8f85d-119">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f85d-119">Windows 2000</span></span>                    | <span data-ttu-id="8f85d-120">1000</span><span class="sxs-lookup"><span data-stu-id="8f85d-120">1000</span></span>                     |
| <span data-ttu-id="8f85d-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f85d-121">Windows Server 2003</span></span>             | <span data-ttu-id="8f85d-122">1.500</span><span class="sxs-lookup"><span data-stu-id="8f85d-122">1500</span></span>                     |



 

<span data-ttu-id="8f85d-123">Para obtener más información sobre cómo recuperar rangos de valores de atributo con ADSI, consulte recuperación de intervalos de [atributos](/windows/desktop/ADSI/attribute-range-retrieval).</span><span class="sxs-lookup"><span data-stu-id="8f85d-123">For more information about retrieving ranges of attribute values with ADSI, see [Attribute Range Retrieval](/windows/desktop/ADSI/attribute-range-retrieval).</span></span>

<span data-ttu-id="8f85d-124">Para obtener más información sobre cómo recuperar intervalos de valores de atributo con [System. DirectoryServices](/dotnet/api/system.directoryservices), consulte [enumeración de miembros en un grupo de gran tamaño](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="8f85d-124">For more information about retrieving ranges of attribute values with [System.DirectoryServices](/dotnet/api/system.directoryservices), see [Enumerating Members in a Large Group](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).</span></span>

 

 