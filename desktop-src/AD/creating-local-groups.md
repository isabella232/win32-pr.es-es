---
title: Crear grupos locales
description: Solo se pueden crear grupos locales para los servidores miembro y Windows 2000 Professional.
ms.assetid: 76cbac51-d8ba-4114-9951-060273be52f3
ms.tgt_platform: multiple
keywords:
- Creación de grupos locales AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705902b0066913fcd6eed56ba7c74e299144595f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104358808"
---
# <a name="creating-local-groups"></a><span data-ttu-id="43770-104">Crear grupos locales</span><span class="sxs-lookup"><span data-stu-id="43770-104">Creating Local Groups</span></span>

<span data-ttu-id="43770-105">Solo se pueden crear grupos locales para los servidores miembro y Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="43770-105">Only local groups can be created for member servers and Windows 2000 Professional.</span></span>

<span data-ttu-id="43770-106">**Para crear un grupo local para un servidor miembro o un equipo que ejecute Windows 2000 Professional**</span><span class="sxs-lookup"><span data-stu-id="43770-106">**To create a local group for a member server or computer running Windows 2000 Professional**</span></span>

1.  <span data-ttu-id="43770-107">Enlazar al equipo mediante las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="43770-107">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="43770-108">Use una cuenta con derechos suficientes para tener acceso a ese equipo.</span><span class="sxs-lookup"><span data-stu-id="43770-108">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="43770-109">Use el siguiente formato de cadena de enlace con el proveedor de WinNT, el nombre del equipo y un parámetro adicional para indicar a ADSI que está enlazando a un equipo: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="43770-109">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span>

        <span data-ttu-id="43770-110">El &lt; parámetro "nombre &gt; de equipo" es el nombre de los grupos de equipos a los que se va a obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="43770-110">The "&lt;computer name&gt;" parameter is the name of the computer groups to access.</span></span>

        <span data-ttu-id="43770-111">En la cadena de enlace, el &lt; parámetro "equipo &gt; " indica a ADSI que está enlazando a un equipo.</span><span class="sxs-lookup"><span data-stu-id="43770-111">In the binding string, the "&lt;computer&gt;" parameter instructs ADSI that it is binding to a computer.</span></span> <span data-ttu-id="43770-112">ADSI hace que estos datos estén disponibles para el analizador del proveedor de WinNT, de modo que pueda omitir algunas consultas de resolución de ambigüedades para determinar el tipo de objeto al que se está enlazando.</span><span class="sxs-lookup"><span data-stu-id="43770-112">ADSI makes this data available to the WinNT provider's parser so that it can skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>

    3.  <span data-ttu-id="43770-113">Enlazar a la interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="43770-113">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>

2.  <span data-ttu-id="43770-114">Especifique "localGroup" como clase mediante [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) para agregar el grupo.</span><span class="sxs-lookup"><span data-stu-id="43770-114">Specify "localGroup" as the class using [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) to add the group.</span></span>
    > [!Note]  
    > <span data-ttu-id="43770-115">Si especifica "Group" como la clase, ADSI utiliza "localGroup".</span><span class="sxs-lookup"><span data-stu-id="43770-115">If you specify "group" as the class, ADSI uses "localGroup".</span></span> <span data-ttu-id="43770-116">No especifique la clase como "globalGroup".</span><span class="sxs-lookup"><span data-stu-id="43770-116">Do not specify the class as "globalGroup".</span></span> <span data-ttu-id="43770-117">No se pueden crear grupos de la clase "globalGroup" en los servidores miembro o en un equipo que ejecute Windows NT Workstation/Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="43770-117">Groups of class "globalGroup" cannot be created on member servers or a computer running Windows NT Workstation/Windows 2000 Professional.</span></span> <span data-ttu-id="43770-118">Si especifica "globalGroup", [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) crea el grupo en la caché de propiedades, pero [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) no escribe el grupo en la base de datos de seguridad y no devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="43770-118">If you specify "globalGroup", [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) creates the group in the property cache, but [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) does not write the group to the security database and it does not return an error.</span></span>

     

3.  <span data-ttu-id="43770-119">Escriba el grupo en la base de datos de seguridad del equipo mediante [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span><span class="sxs-lookup"><span data-stu-id="43770-119">Write the group to the computer security database using [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 