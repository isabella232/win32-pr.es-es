---
title: Atributos (AD DS)
description: Cada objeto de Active Directory Domain Services contiene un conjunto de atributos que definen las características del objeto.
ms.assetid: 9efa7ae1-b6a9-4b95-b031-b502772c536c
ms.tgt_platform: multiple
keywords:
- AD de atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56579494cdc12c2d0ad6fadbb6395d07eaec80d2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077566"
---
# <a name="attributes-ad-ds"></a><span data-ttu-id="59358-104">Atributos (AD DS)</span><span class="sxs-lookup"><span data-stu-id="59358-104">Attributes (AD DS)</span></span>

<span data-ttu-id="59358-105">Cada objeto de Active Directory Domain Services contiene un conjunto de atributos que definen las características del objeto.</span><span class="sxs-lookup"><span data-stu-id="59358-105">Each object in Active Directory Domain Services contains a set of attributes that define the characteristics of the object.</span></span> <span data-ttu-id="59358-106">Cada atributo se describe mediante un objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) en el contenedor de esquemas que define el atributo.</span><span class="sxs-lookup"><span data-stu-id="59358-106">Each attribute is described by an [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object in the schema container that defines the attribute.</span></span> <span data-ttu-id="59358-107">La definición del atributo incluye una variedad de datos, por ejemplo, los tipos de objetos a los que se aplica el atributo y el tipo de sintaxis del atributo.</span><span class="sxs-lookup"><span data-stu-id="59358-107">The attribute definition includes a variety of data, for example, what object types that the attribute applies to and the syntax type of the attribute.</span></span> <span data-ttu-id="59358-108">Para obtener más información acerca de las definiciones de esquema de atributo, vea [características de los atributos](characteristics-of-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="59358-108">For more information about attribute schema definitions, see [Characteristics of Attributes](characteristics-of-attributes.md).</span></span>

<span data-ttu-id="59358-109">En la lista siguiente se enumeran los tipos de atributos que se almacenan en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="59358-109">The following list lists the type of attributes that are stored in Active Directory Domain Services.</span></span>

<dl> <dt>

<span data-ttu-id="59358-110"><span id="Domain-replicated__stored_attributes"></span><span id="domain-replicated__stored_attributes"></span><span id="DOMAIN-REPLICATED__STORED_ATTRIBUTES"></span>Atributos almacenados de dominio replicado</span><span class="sxs-lookup"><span data-stu-id="59358-110"><span id="Domain-replicated__stored_attributes"></span><span id="domain-replicated__stored_attributes"></span><span id="DOMAIN-REPLICATED__STORED_ATTRIBUTES"></span>Domain-replicated, stored attributes</span></span>
</dt> <dd>

<span data-ttu-id="59358-111">Algunos atributos se almacenan en el directorio (por ejemplo, [**CN**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)y [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)) y se replican en todos los controladores de dominio de un dominio.</span><span class="sxs-lookup"><span data-stu-id="59358-111">Some attributes are stored in the directory (such as [**cn**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), and [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)) and replicated to all domain controllers in a domain.</span></span> <span data-ttu-id="59358-112">Un subconjunto de estos atributos también se replica en el catálogo global.</span><span class="sxs-lookup"><span data-stu-id="59358-112">A subset of these attributes is also replicated to the global catalog.</span></span> <span data-ttu-id="59358-113">Si se enumeran los atributos de un objeto desde el catálogo global, solo se devuelven los atributos replicados en el catálogo global.</span><span class="sxs-lookup"><span data-stu-id="59358-113">If you enumerate attributes of an object from the global catalog, only the attributes replicated to the global catalog are returned.</span></span> <span data-ttu-id="59358-114">Algunos atributos también se indizan porque al incluir una propiedad indizada en una consulta, se mejora el rendimiento de las consultas.</span><span class="sxs-lookup"><span data-stu-id="59358-114">Some attributes are also indexed because including an indexed property in a query improves the query performance.</span></span>

</dd> <dt>

<span data-ttu-id="59358-115"><span id="Non-replicated__locally_stored_attributes"></span><span id="non-replicated__locally_stored_attributes"></span><span id="NON-REPLICATED__LOCALLY_STORED_ATTRIBUTES"></span>Atributos almacenados localmente y no replicados</span><span class="sxs-lookup"><span data-stu-id="59358-115"><span id="Non-replicated__locally_stored_attributes"></span><span id="non-replicated__locally_stored_attributes"></span><span id="NON-REPLICATED__LOCALLY_STORED_ATTRIBUTES"></span>Non-replicated, locally stored attributes</span></span>
</dt> <dd>

<span data-ttu-id="59358-116">Los atributos no replicados, como [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**último inicio de sesión**](/windows/desktop/ADSchema/a-lastlogon)y [**último cierre**](/windows/desktop/ADSchema/a-lastlogoff) de sesión se almacenan en cada controlador de dominio, pero no se replican.</span><span class="sxs-lookup"><span data-stu-id="59358-116">Non-replicated attributes, such as [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**Last-Logon**](/windows/desktop/ADSchema/a-lastlogon), and [**Last-Logoff**](/windows/desktop/ADSchema/a-lastlogoff) are stored on each domain controller, but are not replicated.</span></span> <span data-ttu-id="59358-117">Los atributos no replicados son atributos que pertenecen a un controlador de dominio determinado.</span><span class="sxs-lookup"><span data-stu-id="59358-117">The non-replicated attributes are attributes that pertain to a particular domain controller.</span></span> <span data-ttu-id="59358-118">Por ejemplo, el atributo **Last-Logon** es la última fecha y hora en que el inicio de sesión de red del usuario fue validado por el controlador de dominio concreto que devolvió la propiedad.</span><span class="sxs-lookup"><span data-stu-id="59358-118">For example, **Last-Logon** attribute is the last date and time that the user's network logon was validated by that particular domain controller that returned the property.</span></span> <span data-ttu-id="59358-119">Estos atributos se pueden recuperar de la misma manera que los atributos de todo el dominio descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="59358-119">These attributes can be retrieved in the same way as the domain-wide attributes described previously.</span></span> <span data-ttu-id="59358-120">Sin embargo, para estos atributos, cada controlador de dominio solo almacena los valores pertenecientes a ese controlador de dominio en particular.</span><span class="sxs-lookup"><span data-stu-id="59358-120">However, for these attributes, each domain controller stores only values that pertain to that particular domain controller.</span></span> <span data-ttu-id="59358-121">Por ejemplo, para obtener la última vez que un usuario inició sesión en el dominio, recupere el último atributo de **Inicio de sesión** del usuario de cada controlador de dominio en el dominio y busque la última fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="59358-121">For example, to obtain the last time that a user logged on to the domain, retrieve the **Last-Logon** attribute for the user from every domain controller in the domain and find that latest date and time.</span></span>

</dd> <dt>

<span data-ttu-id="59358-122"><span id="Non-stored__constructed_attributes"></span><span id="non-stored__constructed_attributes"></span><span id="NON-STORED__CONSTRUCTED_ATTRIBUTES"></span>Atributos no almacenados y construidos</span><span class="sxs-lookup"><span data-stu-id="59358-122"><span id="Non-stored__constructed_attributes"></span><span id="non-stored__constructed_attributes"></span><span id="NON-STORED__CONSTRUCTED_ATTRIBUTES"></span>Non-stored, constructed attributes</span></span>
</dt> <dd>

<span data-ttu-id="59358-123">Un objeto de usuario también ha construido atributos que no están almacenados en el directorio, pero se calculan mediante el controlador de dominio, como [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) y [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes).</span><span class="sxs-lookup"><span data-stu-id="59358-123">A user object also has constructed attributes that are not stored in the directory, but are calculated by the domain controller, such as [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) and [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes).</span></span>

</dd> </dl>

 

 