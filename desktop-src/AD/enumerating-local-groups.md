---
title: Enumerar grupos locales
description: En los servidores miembro y equipos que ejecutan Windows 2000 Professional, puede enumerar todos los grupos locales.
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- Enumerar los grupos locales AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e106fc2517cfedd8fb5fa40e4b99798ee32de8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789567"
---
# <a name="enumerating-local-groups"></a><span data-ttu-id="5907e-104">Enumerar grupos locales</span><span class="sxs-lookup"><span data-stu-id="5907e-104">Enumerating Local Groups</span></span>

<span data-ttu-id="5907e-105">En los servidores miembro y equipos que ejecutan Windows 2000 Professional, puede enumerar todos los grupos locales.</span><span class="sxs-lookup"><span data-stu-id="5907e-105">On member servers and computers running on Windows 2000 Professional, you can enumerate all local groups.</span></span>

<span data-ttu-id="5907e-106">Solo se pueden crear grupos locales en servidores miembro y Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5907e-106">Only local groups can be created on member servers and Windows 2000 Professional.</span></span> <span data-ttu-id="5907e-107">Sin embargo, esos grupos locales pueden contener:</span><span class="sxs-lookup"><span data-stu-id="5907e-107">However, those local groups can contain:</span></span>

-   <span data-ttu-id="5907e-108">Grupos universales y globales del bosque que contiene el dominio al que pertenece el equipo.</span><span class="sxs-lookup"><span data-stu-id="5907e-108">Universal and Global groups from the forest that contains the domain to which the computer is a member.</span></span>
-   <span data-ttu-id="5907e-109">Grupos locales de dominio del dominio del equipo.</span><span class="sxs-lookup"><span data-stu-id="5907e-109">Domain local groups from that computer's domain.</span></span>
-   <span data-ttu-id="5907e-110">Usuarios de cualquier dominio del bosque.</span><span class="sxs-lookup"><span data-stu-id="5907e-110">Users from any domain in the forest.</span></span>

<span data-ttu-id="5907e-111">**Para enumerar los grupos locales en un servidor miembro o un equipo que ejecuta Windows 2000 Professional**</span><span class="sxs-lookup"><span data-stu-id="5907e-111">**To enumerate the local groups on a member server or computer running Windows 2000 Professional**</span></span>

1.  <span data-ttu-id="5907e-112">Enlazar al equipo mediante las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="5907e-112">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="5907e-113">Use una cuenta con derechos suficientes para tener acceso a ese equipo.</span><span class="sxs-lookup"><span data-stu-id="5907e-113">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="5907e-114">Use el siguiente formato de cadena de enlace con el proveedor de WinNT, el nombre del equipo y un parámetro adicional para indicar a ADSI que está enlazando a un equipo: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="5907e-114">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span>

        <span data-ttu-id="5907e-115">El parámetro "el <computer name> " es el nombre del grupo de equipos al que se va a obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="5907e-115">"The <computer name>" parameter is the name of the computer group to access.</span></span> <span data-ttu-id="5907e-116">Este parámetro indica a ADSI que se enlaza a un equipo y permite que el analizador del proveedor de WinNT omita algunas consultas de resolución de ambigüedades para determinar el tipo de objeto al que se está enlazando.</span><span class="sxs-lookup"><span data-stu-id="5907e-116">This parameter instruct ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>

    3.  <span data-ttu-id="5907e-117">Enlazar a la interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="5907e-117">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>

2.  <span data-ttu-id="5907e-118">Establezca un filtro que contenga "groups" mediante la propiedad [**IADsContainer. Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="5907e-118">Set a filter that contains "groups" using the [**IADsContainer.Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) property.</span></span> <span data-ttu-id="5907e-119">Esto le permite enumerar el contenedor y recuperar solo los grupos.</span><span class="sxs-lookup"><span data-stu-id="5907e-119">This enables you to enumerate the container and retrieve only groups.</span></span>
3.  <span data-ttu-id="5907e-120">Enumerar los objetos de grupo mediante el método [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) .</span><span class="sxs-lookup"><span data-stu-id="5907e-120">Enumerate the group objects, using the [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) method.</span></span>
4.  <span data-ttu-id="5907e-121">Para cada objeto de grupo, use la interfaz [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) para leer el nombre y los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="5907e-121">For each the group object, use the [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) interface to read the name and members of the group.</span></span>

 

 