---
title: Conexión a Active Directory
description: Hay varios métodos que se usan para tener acceso a Active Directory.
ms.assetid: ef5720ff-6c66-466c-967e-f9c72a7bc0fa
ms.tgt_platform: multiple
keywords:
- Conectarse a Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7626f01b644a0bb1a3acb39c5ef5ead70434e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993865"
---
# <a name="connecting-to-active-directory"></a><span data-ttu-id="b1cd7-104">Conexión a Active Directory</span><span class="sxs-lookup"><span data-stu-id="b1cd7-104">Connecting to Active Directory</span></span>

<span data-ttu-id="b1cd7-105">Hay varios métodos que se usan para tener acceso a Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b1cd7-105">There are several methods used to access Active Directory.</span></span> <span data-ttu-id="b1cd7-106">Se recomienda usar la API ADSI para tener acceso a Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b1cd7-106">It is recommended that you use the ADSI API to access Active Directory.</span></span> <span data-ttu-id="b1cd7-107">ADSI implementa el protocolo LDAP para comunicarse con Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b1cd7-107">ADSI implements the LDAP protocol to communicate with Active Directory.</span></span> <span data-ttu-id="b1cd7-108">En los siguientes ejemplos de código se muestra cómo obtener acceso a Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b1cd7-108">The following code examples show how to access Active Directory.</span></span>


```VB
Set ns = GetObject("LDAP:")
```



<span data-ttu-id="b1cd7-109">Esto abre el proveedor LDAP y lo prepara para recuperar los datos.</span><span class="sxs-lookup"><span data-stu-id="b1cd7-109">This opens the LDAP provider and prepares it to retrieve data.</span></span> <span data-ttu-id="b1cd7-110">No se establece ninguna conexión hasta que se soliciten los datos.</span><span class="sxs-lookup"><span data-stu-id="b1cd7-110">No connection is established until data is requested.</span></span> <span data-ttu-id="b1cd7-111">Cuando se solicitan datos, ADSI, con la ayuda del servicio de ubicación, intenta encontrar el mejor controlador de dominio (DC) para la conexión y establecerá una conexión con el servidor.</span><span class="sxs-lookup"><span data-stu-id="b1cd7-111">When data is requested, ADSI, with the help of the locator service, attempts to find the best domain controller (DC) for the connection and will establish a connection to the server.</span></span> <span data-ttu-id="b1cd7-112">Este proceso se conoce como enlace sin servidor.</span><span class="sxs-lookup"><span data-stu-id="b1cd7-112">This process is known as serverless binding.</span></span>

<span data-ttu-id="b1cd7-113">ADSI también permite especificar el nombre del servidor que se va a utilizar para la conexión.</span><span class="sxs-lookup"><span data-stu-id="b1cd7-113">ADSI also enables you to specify the server name to use for the connection.</span></span>


```VB
Set obj = GetObject("LDAP://mysrv01")
```



<span data-ttu-id="b1cd7-114">En otro escenario, es posible que solo conozca el nombre de dominio, pero no el nombre de servidor específico.</span><span class="sxs-lookup"><span data-stu-id="b1cd7-114">In another scenario, you may only know the domain name but not the specific server name.</span></span> <span data-ttu-id="b1cd7-115">De nuevo, ADSI le permite especificar el nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="b1cd7-115">Again, ADSI enables you to specify the domain name.</span></span> <span data-ttu-id="b1cd7-116">En Windows 2000, el nombre de dominio se representa como un nombre DNS.</span><span class="sxs-lookup"><span data-stu-id="b1cd7-116">In Windows 2000, the domain name is represented as a DNS name.</span></span> <span data-ttu-id="b1cd7-117">Por ejemplo, si Joe Worden, el administrador de red elige conectarse con el nombre de dominio, podría usar el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="b1cd7-117">For example, if Joe Worden, the network administrator, chooses to connect using the domain name, he could use the following code example.</span></span>


```VB
Set obj = GetObject("LDAP://fabrikam.com")
```



<span data-ttu-id="b1cd7-118">ADSI se conectará a uno de los controladores de dominio del dominio fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="b1cd7-118">ADSI will connect to one of the domain controllers in the fabrikam.com domain.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1cd7-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1cd7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1cd7-120">Enlazar a objetos de Active Directory</span><span class="sxs-lookup"><span data-stu-id="b1cd7-120">Binding to Active Directory Objects</span></span>](binding-to-active-directory-objects.md)
</dt> </dl>

 

 




