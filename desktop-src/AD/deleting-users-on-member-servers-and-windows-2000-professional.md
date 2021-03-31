---
title: Eliminación de usuarios en servidores miembro y Windows 2000 Professional
description: En este tema se muestra cómo eliminar un usuario de un servidor miembro o un equipo que ejecuta en Windows 2000 Professional.
ms.assetid: 0c94c08b-46cb-494e-89f8-a21bfb20e34c
ms.tgt_platform: multiple
keywords:
- usuarios AD, eliminación de un usuario en servidores miembro y Windows 2000 Professional
- Active Directory, uso, usuarios, eliminación de usuarios en servidores miembro y Windows 2000 Professional
- eliminación de un usuario
- servidor, eliminación de un usuario
- eliminación de usuarios en servidores miembro y Windows 2000 Professional AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aae4287c8b7d32e15e7df3e73f365409d7fe49a0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077532"
---
# <a name="deleting-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="ca967-108">Eliminación de usuarios en servidores miembro y Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ca967-108">Deleting Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="ca967-109">En este tema se muestra cómo eliminar un usuario de un servidor miembro o un equipo que ejecuta en Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ca967-109">This topic shows how to delete a user from a member server or computer running on Windows 2000 Professional.</span></span>

<span data-ttu-id="ca967-110">**Para eliminar un usuario**</span><span class="sxs-lookup"><span data-stu-id="ca967-110">**To delete a user**</span></span>

1.  <span data-ttu-id="ca967-111">Enlazar al equipo mediante las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="ca967-111">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="ca967-112">Use una cuenta con derechos suficientes para tener acceso a ese equipo.</span><span class="sxs-lookup"><span data-stu-id="ca967-112">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="ca967-113">Use el siguiente formato de cadena de enlace con el proveedor de WinNT, el nombre del equipo y un parámetro adicional para indicar a ADSI que está enlazando a un equipo: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="ca967-113">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to tell ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="ca967-114">El &lt; parámetro "nombre &gt; de equipo" es el nombre del equipo a cuyos grupos desea obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="ca967-114">The "&lt;computer name&gt;" parameter is the name of the computer whose groups you want to access.</span></span> <span data-ttu-id="ca967-115">Este parámetro notifica a ADSI que está enlazando a un equipo y permite al analizador del proveedor de WinNT omitir algunas consultas de resolución de ambigüedades para determinar el tipo de objeto al que se está enlazando.</span><span class="sxs-lookup"><span data-stu-id="ca967-115">This parameter notifies ADSI that it is binding to a computer and allows the WinNT provider parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="ca967-116">Enlazar a la interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="ca967-116">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="ca967-117">Especifique "User" como la clase mediante [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) para eliminar el usuario.</span><span class="sxs-lookup"><span data-stu-id="ca967-117">Specify "user" as the class using [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) to delete the user.</span></span>

    <span data-ttu-id="ca967-118">Tenga en cuenta que no es necesario llamar a [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar el cambio en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="ca967-118">Be aware that you do not need to call [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the change to the container.</span></span> <span data-ttu-id="ca967-119">La llamada [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) confirma la eliminación del usuario directamente en el directorio.</span><span class="sxs-lookup"><span data-stu-id="ca967-119">The [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) call commits the deletion of the user directly to the directory.</span></span>

 

 