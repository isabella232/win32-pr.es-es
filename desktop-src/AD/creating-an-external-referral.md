---
title: Crear una referencia externa
description: Si se crea un objeto crossRef externo y un controlador de dominio lo utiliza para generar una referencia, el objeto crossRef proporciona dos elementos de datos importantes en las siguientes propiedades.
ms.assetid: 9805390c-9e8d-4afd-bffc-43abf6055413
ms.tgt_platform: multiple
keywords:
- referencias externas Active Directory
- Active Directory ejemplos Active Directory, crear una referencia externa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a9306c374a0c22d206e9a0f9dbb8cd240da0c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789592"
---
# <a name="creating-an-external-referral"></a><span data-ttu-id="66702-105">Crear una referencia externa</span><span class="sxs-lookup"><span data-stu-id="66702-105">Creating an External Referral</span></span>

<span data-ttu-id="66702-106">Si se crea un objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) externo y un controlador de dominio lo utiliza para generar una referencia, el objeto **crossRef** proporciona dos elementos de datos importantes en las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="66702-106">If an external [**crossRef**](/windows/desktop/ADSchema/c-crossref) object is created and a domain controller uses it to generate a referral, the **crossRef** object provides two important data elements in the following properties.</span></span> <span data-ttu-id="66702-107">Para obtener más información sobre las situaciones en las que esto puede ocurrir, consulte la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="66702-107">For more information about situations where this can occur, see the previous section.</span></span>



| <span data-ttu-id="66702-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="66702-108">Property</span></span>                           | <span data-ttu-id="66702-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="66702-109">Description</span></span>                                                                                                                                                         |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66702-110">**dnsRoot**</span><span class="sxs-lookup"><span data-stu-id="66702-110">**dnsRoot**</span></span>](/windows/desktop/ADSchema/a-dnsroot) | <span data-ttu-id="66702-111">Especifica el servidor o dominio que puede servir a los datos del contexto de nomenclatura especificado en [**NCName**](/windows/desktop/ADSchema/a-ncname).</span><span class="sxs-lookup"><span data-stu-id="66702-111">Specifies the server or domain that can serve data from the naming context specified in [**nCName**](/windows/desktop/ADSchema/a-ncname).</span></span>                                           |
| [<span data-ttu-id="66702-112">**nCName**</span><span class="sxs-lookup"><span data-stu-id="66702-112">**nCName**</span></span>](/windows/desktop/ADSchema/a-ncname)   | <span data-ttu-id="66702-113">Especifica el nombre distintivo del dominio, el esquema o el contenedor de configuración con raíz en el servidor o dominio especificado por [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot).</span><span class="sxs-lookup"><span data-stu-id="66702-113">Specifies the distinguished name for the domain, schema, or configuration container rooted at the server or domain specified by [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot).</span></span> |



 

<span data-ttu-id="66702-114">Por ejemplo, si el servidor con la dirección DNS de serv1.Northwest.fabrikam.com atiende el contexto de nomenclatura cuya raíz es CN =, ou = MyDOM, O = Fabrikam, establezca [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) en la dirección DNS de ese servidor y el [**NCName**](/windows/desktop/ADSchema/a-ncname) en el nombre distintivo del dominio, el esquema o el contenedor de configuración.</span><span class="sxs-lookup"><span data-stu-id="66702-114">For example, if the server with DNS address of serv1.northwest.Fabrikam.com serves the naming context rooted at CN=MyContainer,OU=MyDOM,O=Fabrikam, set the [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) to that server's DNS address and the [**nCName**](/windows/desktop/ADSchema/a-ncname) to the distinguished name of the domain, schema, or configuration container.</span></span>

<span data-ttu-id="66702-115">Para obtener más información y un ejemplo de código que muestra cómo crear una referencia externa, vea [código de ejemplo para crear un objeto crossRef externo](example-code-for-creating-an-external-crossref-object.md).</span><span class="sxs-lookup"><span data-stu-id="66702-115">For more information and a code example that shows how to create an external referral, see [Example Code for Creating an External crossRef Object](example-code-for-creating-an-external-crossref-object.md).</span></span>

 

 