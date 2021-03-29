---
title: Enlace sin servidor y RootDSE
description: Si es posible, no codifique un nombre de servidor.
ms.assetid: 24cfd8ce-18e6-42f1-8bc5-2c6dee82d133
ms.tgt_platform: multiple
keywords:
- Enlace sin servidor y AD de RootDSE
- Enlace sin servidor AD
- AD de RootDSE
- Active Directory, uso, enlace, enlace sin servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 492a1ed115c4b0d9160305eb54b08c24db86abb8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487403"
---
# <a name="serverless-binding-and-rootdse"></a><span data-ttu-id="86d5f-107">Enlace sin servidor y RootDSE</span><span class="sxs-lookup"><span data-stu-id="86d5f-107">Serverless Binding and RootDSE</span></span>

<span data-ttu-id="86d5f-108">Si es posible, no codifique un nombre de servidor.</span><span class="sxs-lookup"><span data-stu-id="86d5f-108">If possible, do not hard-code a server name.</span></span> <span data-ttu-id="86d5f-109">Además, en la mayoría de los casos, el enlace no debe estar asociado innecesariamente a un solo servidor.</span><span class="sxs-lookup"><span data-stu-id="86d5f-109">Furthermore, under most circumstances, binding should not be unnecessarily tied to a single server.</span></span> <span data-ttu-id="86d5f-110">Active Directory Domain Services admiten el enlace sin servidor, lo que significa que Active Directory se pueden enlazar a en el dominio predeterminado sin especificar el nombre de un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="86d5f-110">Active Directory Domain Services support serverless binding, which means that Active Directory can be bound to on the default domain without specifying the name of a domain controller.</span></span> <span data-ttu-id="86d5f-111">En el caso de las aplicaciones normales, suele ser el dominio del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="86d5f-111">For ordinary applications, this is typically the domain of the logged-on user.</span></span> <span data-ttu-id="86d5f-112">En el caso de las aplicaciones de servicio, es el dominio de la cuenta de inicio de sesión del servicio o el del cliente que suplanta el servicio.</span><span class="sxs-lookup"><span data-stu-id="86d5f-112">For service applications, this is either the domain of the service logon account or that of the client that the service impersonates.</span></span>

<span data-ttu-id="86d5f-113">En LDAP 3,0, rootDSE se define como la raíz del árbol de datos de directorio en un servidor de directorio.</span><span class="sxs-lookup"><span data-stu-id="86d5f-113">In LDAP 3.0, rootDSE is defined as the root of the directory data tree on a directory server.</span></span> <span data-ttu-id="86d5f-114">RootDSE no forma parte de ningún espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="86d5f-114">The rootDSE is not part of any namespace.</span></span> <span data-ttu-id="86d5f-115">El propósito de rootDSE es proporcionar datos sobre el servidor de directorio.</span><span class="sxs-lookup"><span data-stu-id="86d5f-115">The purpose of the rootDSE is to provide data about the directory server.</span></span> <span data-ttu-id="86d5f-116">A continuación se encuentra la cadena de enlace que se utiliza para enlazar a rootDSE.</span><span class="sxs-lookup"><span data-stu-id="86d5f-116">The following is the binding string that is used to bind to rootDSE.</span></span>


```C++
LDAP://<servername>/rootDSE
```



<span data-ttu-id="86d5f-117"><servername>Es el nombre DNS de un servidor.</span><span class="sxs-lookup"><span data-stu-id="86d5f-117">The <servername> is the DNS name of a server.</span></span> <span data-ttu-id="86d5f-118"><servername>Es opcional, como se muestra en el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="86d5f-118">The <servername> is optional, as shown in the following format.</span></span>


```C++
LDAP://rootDSE
```



<span data-ttu-id="86d5f-119">En este caso, se utilizará un controlador de dominio predeterminado del dominio en el que se encuentra el contexto de seguridad del subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="86d5f-119">In this case, a default domain controller from the domain that the security context of the calling thread is in will be used.</span></span> <span data-ttu-id="86d5f-120">Si no se puede tener acceso a un controlador de dominio en el sitio, se utilizará el primer controlador de dominio que se pueda encontrar.</span><span class="sxs-lookup"><span data-stu-id="86d5f-120">If a domain controller cannot be accessed within the site, the first domain controller that can be found will be used.</span></span>

<span data-ttu-id="86d5f-121">RootDSE es una ubicación conocida y confiable en cada servidor de directorio para obtener nombres distintivos de los contenedores de dominio, esquema y configuración, y otros datos sobre el servidor y el contenido de su árbol de datos de directorio.</span><span class="sxs-lookup"><span data-stu-id="86d5f-121">The rootDSE is a well-known and reliable location on every directory server to get distinguished names of the domain, schema, and configuration containers, and other data about the server and the contents of its directory data tree.</span></span> <span data-ttu-id="86d5f-122">Estas propiedades rara vez cambian en un servidor determinado.</span><span class="sxs-lookup"><span data-stu-id="86d5f-122">These properties rarely change on a particular server.</span></span> <span data-ttu-id="86d5f-123">Una aplicación puede leer estas propiedades en el inicio y usarlas en toda la sesión.</span><span class="sxs-lookup"><span data-stu-id="86d5f-123">An application can read these properties at startup and use them throughout the session.</span></span>

<span data-ttu-id="86d5f-124">En Resumen, una aplicación debe usar el enlace sin servidor para enlazar con el directorio en el dominio actual, usar rootDSE para obtener el nombre distintivo de un espacio de nombres y usar ese nombre distintivo para enlazar con los objetos del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="86d5f-124">In summary, an application should use serverless binding to bind to the directory on the current domain, use rootDSE to get the distinguished name for a namespace, and use that distinguished name to bind to objects in the namespace.</span></span>

<span data-ttu-id="86d5f-125">Para obtener más información acerca de los atributos admitidos por rootDSE, consulte [RootDSE](/windows/desktop/ADSchema/rootdse) en la documentación del esquema de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="86d5f-125">For more information about attributes supported by rootDSE, see [RootDSE](/windows/desktop/ADSchema/rootdse) in the Active Directory Schema documentation.</span></span>

<span data-ttu-id="86d5f-126">Para obtener más información y un ejemplo de código que muestra cómo usar el enlace sin servidor y rootDSE, consulte [el código de ejemplo para obtener el nombre distintivo del dominio](example-code-for-getting-the-distinguished-name-of-the-domain.md).</span><span class="sxs-lookup"><span data-stu-id="86d5f-126">For more information and a code example that shows how to use serverless binding and rootDSE, see [Example Code for Getting the Distinguished Name of the Domain](example-code-for-getting-the-distinguished-name-of-the-domain.md).</span></span>

 

 