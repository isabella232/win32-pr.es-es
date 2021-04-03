---
title: Enumerar usuarios en servidores miembro y Windows 2000 Professional
description: En este tema se muestra cómo enumerar todos los usuarios, en una base de datos de seguridad local, en servidores miembro y equipos que ejecutan Windows 2000 Professional.
ms.assetid: 56c20e8a-2861-4cd9-8058-271c89db7ec9
ms.tgt_platform: multiple
keywords:
- Enumerar usuarios en servidores miembro y Windows 2000 Professional AD
- usuarios AD, enumeración de usuarios en servidores miembro y Windows 2000 Professional
- Active Directory, usar, usuarios, enumerar usuarios en servidores miembro y Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664af51b7feb2e0b9a683664659eefda11c9cb9d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789562"
---
# <a name="enumerating-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="797bb-106">Enumerar usuarios en servidores miembro y Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="797bb-106">Enumerating Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="797bb-107">En este tema se muestra cómo enumerar todos los usuarios, en una base de datos de seguridad local, en servidores miembro y equipos que ejecutan Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="797bb-107">This topic shows how to enumerate all users, in a local security database, on member servers and computers running on Windows 2000 Professional.</span></span>

<span data-ttu-id="797bb-108">**Para enumerar los usuarios**</span><span class="sxs-lookup"><span data-stu-id="797bb-108">**To enumerate the users**</span></span>

1.  <span data-ttu-id="797bb-109">Enlazar al equipo mediante las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="797bb-109">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="797bb-110">Use una cuenta que tenga derechos suficientes para acceder a ese equipo.</span><span class="sxs-lookup"><span data-stu-id="797bb-110">Use an account that has sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="797bb-111">Use el siguiente formato de cadena de enlace con el proveedor de WinNT, el nombre del equipo y un parámetro adicional para indicar a ADSI que está enlazando a un equipo: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="797bb-111">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="797bb-112">El &lt; parámetro "nombre &gt; de equipo" es el nombre del equipo para cuyos grupos tienen acceso.</span><span class="sxs-lookup"><span data-stu-id="797bb-112">The "&lt;computer name&gt;" parameter is the name of the computer for whose groups to access.</span></span> <span data-ttu-id="797bb-113">Este parámetro indica a ADSI que se enlaza a un equipo y permite al analizador del proveedor de WinNT omitir algunas consultas de resolución de ambigüedades para determinar el tipo de objeto al que se está enlazando.</span><span class="sxs-lookup"><span data-stu-id="797bb-113">This parameter instructs ADSI that it is binding to a computer and enables the WinNT provider parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="797bb-114">Enlazar a la interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="797bb-114">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="797bb-115">Agregue "User" a la propiedad [**IADsContainer. Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) .</span><span class="sxs-lookup"><span data-stu-id="797bb-115">Add "user" to the [**IADsContainer.Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) property.</span></span> <span data-ttu-id="797bb-116">Esto hace que la enumeración solo contenga objetos que tengan la clase de objeto "User".</span><span class="sxs-lookup"><span data-stu-id="797bb-116">This causes the enumeration to only contain objects that have the "user" object class.</span></span>
3.  <span data-ttu-id="797bb-117">Enumerar los objetos.</span><span class="sxs-lookup"><span data-stu-id="797bb-117">Enumerate the objects.</span></span> <span data-ttu-id="797bb-118">Para cada objeto de usuario, use los métodos de interfaz [**IADs**](/windows/desktop/api/iads/nn-iads-iads) o [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) para leer las propiedades de usuario.</span><span class="sxs-lookup"><span data-stu-id="797bb-118">For each user object, use the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) or [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) interface methods to read the user properties.</span></span>

 

 