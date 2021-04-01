---
title: RootDSE (ADSI)
description: Cada servidor de directorio tiene una entrada única denominada RootDSE. Proporciona datos sobre el servidor, como sus capacidades, la versión de LDAP que admite y los contextos de nomenclatura que usa.
ms.assetid: bb6b7676-7042-453f-83f9-b0dd2e377a13
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f241f2b8bb08248c0579c5c23d461b8c0acf1e01
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793833"
---
# <a name="rootdse-adsi"></a><span data-ttu-id="30fe6-104">RootDSE (ADSI)</span><span class="sxs-lookup"><span data-stu-id="30fe6-104">RootDSE (ADSI)</span></span>

<span data-ttu-id="30fe6-105">Cada servidor de directorio tiene una entrada única denominada **RootDSE**.</span><span class="sxs-lookup"><span data-stu-id="30fe6-105">Each directory server has a unique entry called **RootDSE**.</span></span> <span data-ttu-id="30fe6-106">Proporciona datos sobre el servidor, como sus capacidades, la versión de LDAP que admite y los contextos de nomenclatura que usa.</span><span class="sxs-lookup"><span data-stu-id="30fe6-106">It provides data about the server, such as its capabilities, the LDAP version it supports, and the naming contexts it uses.</span></span>

<span data-ttu-id="30fe6-107">Por ejemplo, para crear un script, o una aplicación, que se pueda ejecutar en cualquier entorno de dominio de Windows.</span><span class="sxs-lookup"><span data-stu-id="30fe6-107">For example, to create a script, or application, that can run on any Windows domain environment.</span></span> <span data-ttu-id="30fe6-108">Puede especificar el nombre distintivo, el nombre del servidor o el nombre de dominio al conectarse a Active Directory.</span><span class="sxs-lookup"><span data-stu-id="30fe6-108">You can specify either the distinguished name, server name, or domain name when connecting to Active Directory.</span></span> <span data-ttu-id="30fe6-109">Si no dispone de esta información, puede usar el objeto **RootDSE** para establecer una conexión.</span><span class="sxs-lookup"><span data-stu-id="30fe6-109">If you do not have this information, you can then use the **RootDSE** object to establish a connection.</span></span> <span data-ttu-id="30fe6-110">En el siguiente ejemplo de código se cambia la descripción del dominio en cualquier dominio.</span><span class="sxs-lookup"><span data-stu-id="30fe6-110">The following code example changes the domain description in any domain.</span></span>


```VB
Set rootDSE = GetObject("LDAP://RootDSE")
Set dom = GetObject( "LDAP://" & rootDSE.Get("defaultNamingContext"))
dom.Put "description", "My domain"
dom.SetInfo
```



<span data-ttu-id="30fe6-111">Al obtener el atributo **defaultNamingContext** de **RootDSE**, puede enlazar con el dominio actual; por ejemplo, Fabrikam **defaultNamingContext** es DC = Fabrikam, DC = com.</span><span class="sxs-lookup"><span data-stu-id="30fe6-111">By getting the **defaultNamingContext** attribute from **RootDSE**, you can bind to the current domain, for example, the Fabrikam **defaultNamingContext** is DC=Fabrikam, DC=COM.</span></span>

<span data-ttu-id="30fe6-112">Para enumerar las propiedades de **RootDSE**, use la interfaz [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) .</span><span class="sxs-lookup"><span data-stu-id="30fe6-112">To enumerate the properties of the **RootDSE**, use the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface.</span></span> <span data-ttu-id="30fe6-113">No se puede usar [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para esta tarea.</span><span class="sxs-lookup"><span data-stu-id="30fe6-113">[**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) cannot be used for this task.</span></span>

<span data-ttu-id="30fe6-114">Para obtener más información, vea [enlace sin servidor y RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).</span><span class="sxs-lookup"><span data-stu-id="30fe6-114">For more information, see [Serverless Binding and RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).</span></span>

 

 