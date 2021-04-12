---
title: Eliminar grupos locales
description: En este tema se muestra cómo eliminar un grupo local de un servidor miembro o un equipo que ejecuta en Windows 2000 Professional.
ms.assetid: 030da25a-a606-4521-a243-d902c772fd00
ms.tgt_platform: multiple
keywords:
- Eliminar grupos locales AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b55f90a8e6ac5cb77bf878d5ac680a6da91f73
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487463"
---
# <a name="deleting-local-groups"></a><span data-ttu-id="fa718-104">Eliminar grupos locales</span><span class="sxs-lookup"><span data-stu-id="fa718-104">Deleting Local Groups</span></span>

<span data-ttu-id="fa718-105">En este tema se muestra cómo eliminar un grupo local de un servidor miembro o un equipo que ejecuta en Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="fa718-105">This topic shows how to delete a local group from a member server or computer running on Windows 2000 Professional.</span></span>

<span data-ttu-id="fa718-106">**Para eliminar un grupo local**</span><span class="sxs-lookup"><span data-stu-id="fa718-106">**To delete a local group**</span></span>

1.  <span data-ttu-id="fa718-107">Enlazar al equipo mediante las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="fa718-107">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="fa718-108">Use una cuenta con derechos suficientes para tener acceso a ese equipo.</span><span class="sxs-lookup"><span data-stu-id="fa718-108">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="fa718-109">Use el siguiente formato de cadena de enlace con el proveedor de WinNT, el nombre del equipo y un parámetro adicional para indicar a ADSI que está enlazando a un equipo: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="fa718-109">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="fa718-110">El &lt; parámetro "nombre &gt; de equipo" es el nombre del grupo de equipos al que se va a obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="fa718-110">The "&lt;computer name&gt;" parameter is the name of the computer group to access.</span></span> <span data-ttu-id="fa718-111">Este parámetro indica a ADSI que se enlaza a un equipo y permite que el analizador del proveedor de WinNT omita algunas consultas de resolución de ambigüedades para determinar el tipo de objeto al que se está enlazando.</span><span class="sxs-lookup"><span data-stu-id="fa718-111">This parameter instruct ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="fa718-112">Enlazar a la interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="fa718-112">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="fa718-113">Especifique "Group" como la clase mediante [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)para eliminar el grupo.</span><span class="sxs-lookup"><span data-stu-id="fa718-113">Specify "group" as the class using [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)to delete the group.</span></span>

    <span data-ttu-id="fa718-114">No es necesario llamar a [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar el cambio en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="fa718-114">You do not need to call [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the change to the container.</span></span> <span data-ttu-id="fa718-115">La llamada [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) confirma la eliminación del grupo directamente en el directorio.</span><span class="sxs-lookup"><span data-stu-id="fa718-115">The [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) call commits the deletion of the group directly to the directory.</span></span>

 

 