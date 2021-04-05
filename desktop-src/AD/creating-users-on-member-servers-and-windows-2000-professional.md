---
title: Creación de usuarios en servidores miembro y Windows 2000 Professional
description: En este tema se describen los pasos que se usan para crear un usuario en un servidor miembro o en un equipo que ejecuta Windows 2000 Professional.
ms.assetid: 714a36d4-3407-426f-b4e9-27ec399f742a
ms.tgt_platform: multiple
keywords:
- Crear usuarios en servidores miembro y Windows 2000 Professional AD
- usuarios AD, creación de un usuario en servidores miembro y Windows 2000 Professional
- Active Directory, uso, usuarios, creación de un usuario en servidores miembro y Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050c9e8ecf68465097f2c185d2d31e0195c25a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077540"
---
# <a name="creating-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="7a879-106">Creación de usuarios en servidores miembro y Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7a879-106">Creating Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="7a879-107">**Para crear un usuario**</span><span class="sxs-lookup"><span data-stu-id="7a879-107">**To create a user**</span></span>

1.  <span data-ttu-id="7a879-108">Enlazar al equipo mediante las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="7a879-108">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="7a879-109">Use una cuenta que tenga derechos suficientes para acceder a ese equipo.</span><span class="sxs-lookup"><span data-stu-id="7a879-109">Use an account that has sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="7a879-110">Use el siguiente formato de cadena de enlace con el proveedor de WinNT, el nombre del equipo y un parámetro adicional para indicar a ADSI que está enlazando a un equipo: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="7a879-110">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to tell ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="7a879-111">El &lt; equipo "nombre &gt; de equipo" es el nombre del equipo a cuyos grupos desea obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="7a879-111">The "&lt;computer name&gt;" computer is the name of the computer whose groups you want to access.</span></span> <span data-ttu-id="7a879-112">Este parámetro indica a ADSI que se enlaza a un equipo y permite que el analizador del proveedor de WinNT omita algunas consultas de resolución de ambigüedades para determinar el tipo de objeto al que se está enlazando.</span><span class="sxs-lookup"><span data-stu-id="7a879-112">This parameter tells ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="7a879-113">Enlazar a la interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="7a879-113">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="7a879-114">Especifique "User" como la clase mediante [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) para agregar el usuario.</span><span class="sxs-lookup"><span data-stu-id="7a879-114">Specify "user" as the class using [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) to add the user.</span></span>
3.  <span data-ttu-id="7a879-115">Escriba el usuario en la base de datos de seguridad del equipo mediante [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span><span class="sxs-lookup"><span data-stu-id="7a879-115">Write the user to the computer's security database using [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 