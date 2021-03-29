---
description: Puede usar la interfaz IX500DistinguishedName para crear un nombre de sujeto a partir de una cadena de nombre distintivo.
ms.assetid: 78fbf15a-678f-4d87-a309-e70374e3ecee
title: Crear un nombre de sujeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe512be48c9a727857c4fac4abc6e04a705b7f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540155"
---
# <a name="creating-a-subject-name"></a><span data-ttu-id="23e06-103">Crear un nombre de sujeto</span><span class="sxs-lookup"><span data-stu-id="23e06-103">Creating a Subject Name</span></span>

<span data-ttu-id="23e06-104">Puede usar la interfaz [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) para crear un nombre de sujeto a partir de una cadena de nombre distintivo.</span><span class="sxs-lookup"><span data-stu-id="23e06-104">You can use the [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) interface to create a subject name from a distinguished name string.</span></span> <span data-ttu-id="23e06-105">La cadena consta de nombres distintivos relativos (RDN) concatenados.</span><span class="sxs-lookup"><span data-stu-id="23e06-105">The string consists of concatenated relative distinguished names (RDNs).</span></span> <span data-ttu-id="23e06-106">Las siguientes claves RDN son compatibles con la API de inscripción de certificados.</span><span class="sxs-lookup"><span data-stu-id="23e06-106">The following RDN keys are supported by the Certificate Enrollment API.</span></span>

| <span data-ttu-id="23e06-107">Clave</span><span class="sxs-lookup"><span data-stu-id="23e06-107">Key</span></span>                               | <span data-ttu-id="23e06-108">OID</span><span class="sxs-lookup"><span data-stu-id="23e06-108">OID</span></span>                                             | <span data-ttu-id="23e06-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="23e06-109">Description</span></span>                                                                                        |
|-----------------------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23e06-110">C</span><span class="sxs-lookup"><span data-stu-id="23e06-110">C</span></span><br/>                      | <span data-ttu-id="23e06-111">XCN \_ \_ nombre del país OID \_</span><span class="sxs-lookup"><span data-stu-id="23e06-111">XCN\_OID\_COUNTRY\_NAME</span></span><br/>              | <span data-ttu-id="23e06-112">Contiene un código de país o región ISO 3166 de dos letras.</span><span class="sxs-lookup"><span data-stu-id="23e06-112">Contains a two-letter ISO 3166 country or region code.</span></span><br/>                                  |
| <span data-ttu-id="23e06-113">CN</span><span class="sxs-lookup"><span data-stu-id="23e06-113">CN</span></span><br/>                     | <span data-ttu-id="23e06-114">\_ \_ nombre común de OID de XCN \_</span><span class="sxs-lookup"><span data-stu-id="23e06-114">XCN\_OID\_COMMON\_NAME</span></span><br/>               | <span data-ttu-id="23e06-115">Contiene un nombre común.</span><span class="sxs-lookup"><span data-stu-id="23e06-115">Contains a common name.</span></span><br/>                                                                 |
| <span data-ttu-id="23e06-116">E</span><span class="sxs-lookup"><span data-stu-id="23e06-116">E</span></span><br/> <span data-ttu-id="23e06-117">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="23e06-117">EMAIL</span></span><br/>     | <span data-ttu-id="23e06-118">XCN \_ OID \_ RSA \_ emailAddr</span><span class="sxs-lookup"><span data-stu-id="23e06-118">XCN\_OID\_RSA\_emailAddr</span></span><br/>             | <span data-ttu-id="23e06-119">Contiene una dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="23e06-119">Contains an email address.</span></span><br/>                                                              |
| <span data-ttu-id="23e06-120">DC</span><span class="sxs-lookup"><span data-stu-id="23e06-120">DC</span></span><br/>                     | <span data-ttu-id="23e06-121">\_componente de \_ dominio \_ OID de XCN</span><span class="sxs-lookup"><span data-stu-id="23e06-121">XCN\_OID\_DOMAIN\_COMPONENT</span></span><br/>          | <span data-ttu-id="23e06-122">Contiene una parte de un nombre DNS (sistema de nombres de dominio).</span><span class="sxs-lookup"><span data-stu-id="23e06-122">Contains one part of a Domain Name System (DNS) name.</span></span><br/>                                   |
| <span data-ttu-id="23e06-123">G</span><span class="sxs-lookup"><span data-stu-id="23e06-123">G</span></span><br/> <span data-ttu-id="23e06-124">GivenName</span><span class="sxs-lookup"><span data-stu-id="23e06-124">GivenName</span></span><br/> | <span data-ttu-id="23e06-125">\_nombre XCN OID \_ proporcionado \_</span><span class="sxs-lookup"><span data-stu-id="23e06-125">XCN\_OID\_GIVEN\_NAME</span></span><br/>                | <span data-ttu-id="23e06-126">Contiene la parte del nombre de una persona que no es un apellido.</span><span class="sxs-lookup"><span data-stu-id="23e06-126">Contains the part of a person's name that is not a surname.</span></span><br/>                             |
| <span data-ttu-id="23e06-127">I</span><span class="sxs-lookup"><span data-stu-id="23e06-127">I</span></span><br/>                      | <span data-ttu-id="23e06-128">iniciales de XCN \_ OID \_</span><span class="sxs-lookup"><span data-stu-id="23e06-128">XCN\_OID\_INITIALS</span></span><br/>                   | <span data-ttu-id="23e06-129">Contiene las iniciales de una persona.</span><span class="sxs-lookup"><span data-stu-id="23e06-129">Contains a person's initials.</span></span><br/>                                                           |
| <span data-ttu-id="23e06-130">L</span><span class="sxs-lookup"><span data-stu-id="23e06-130">L</span></span><br/>                      | <span data-ttu-id="23e06-131">XCN \_ nombre de la localidad del OID \_ \_</span><span class="sxs-lookup"><span data-stu-id="23e06-131">XCN\_OID\_LOCALITY\_NAME</span></span><br/>             | <span data-ttu-id="23e06-132">Contiene el nombre de la localidad que identifica una ciudad, un país u otra región geográfica.</span><span class="sxs-lookup"><span data-stu-id="23e06-132">Contains the locality name that identifies a city, country, or other geographic region.</span></span><br/> |
| <span data-ttu-id="23e06-133">O</span><span class="sxs-lookup"><span data-stu-id="23e06-133">O</span></span><br/>                      | <span data-ttu-id="23e06-134">XCN \_ nombre de la \_ organización OID \_</span><span class="sxs-lookup"><span data-stu-id="23e06-134">XCN\_OID\_ORGANIZATION\_NAME</span></span><br/>         | <span data-ttu-id="23e06-135">Contiene el nombre de una organización.</span><span class="sxs-lookup"><span data-stu-id="23e06-135">Contains the name of an organization.</span></span><br/>                                                   |
| <span data-ttu-id="23e06-136">OU</span><span class="sxs-lookup"><span data-stu-id="23e06-136">OU</span></span><br/>                     | <span data-ttu-id="23e06-137">\_nombre de \_ \_ unidad organizativa XCN OID \_</span><span class="sxs-lookup"><span data-stu-id="23e06-137">XCN\_OID\_ORGANIZATIONAL\_UNIT\_NAME</span></span><br/> | <span data-ttu-id="23e06-138">Contiene el nombre de una subdivisión de unidad dentro de una organización.</span><span class="sxs-lookup"><span data-stu-id="23e06-138">Contains the name of a unit subdivision within an organization.</span></span><br/>                         |
| <span data-ttu-id="23e06-139">S</span><span class="sxs-lookup"><span data-stu-id="23e06-139">S</span></span><br/> <span data-ttu-id="23e06-140">ST</span><span class="sxs-lookup"><span data-stu-id="23e06-140">ST</span></span><br/>        | <span data-ttu-id="23e06-141">XCN \_ \_ \_ nombre de estado o \_ provincia de \_ OID</span><span class="sxs-lookup"><span data-stu-id="23e06-141">XCN\_OID\_STATE\_OR\_PROVINCE\_NAME</span></span><br/>  | <span data-ttu-id="23e06-142">Contiene el nombre completo de un estado o provincia.</span><span class="sxs-lookup"><span data-stu-id="23e06-142">Contains the full name of a state or province.</span></span><br/>                                          |
| <span data-ttu-id="23e06-143">STREET</span><span class="sxs-lookup"><span data-stu-id="23e06-143">STREET</span></span><br/>                 | <span data-ttu-id="23e06-144">\_Dirección XCN \_ OID \_</span><span class="sxs-lookup"><span data-stu-id="23e06-144">XCN\_OID\_STREET\_ADDRESS</span></span><br/>            | <span data-ttu-id="23e06-145">Contiene la dirección física.</span><span class="sxs-lookup"><span data-stu-id="23e06-145">Contains the physical address.</span></span><br/>                                                          |
| <span data-ttu-id="23e06-146">SN</span><span class="sxs-lookup"><span data-stu-id="23e06-146">SN</span></span><br/>                     | <span data-ttu-id="23e06-147">nombre de XCN \_ OID \_ sur \_</span><span class="sxs-lookup"><span data-stu-id="23e06-147">XCN\_OID\_SUR\_NAME</span></span><br/>                  | <span data-ttu-id="23e06-148">Contiene el nombre de familia de una persona.</span><span class="sxs-lookup"><span data-stu-id="23e06-148">Contains the family name of a person.</span></span><br/>                                                   |
| <span data-ttu-id="23e06-149">T</span><span class="sxs-lookup"><span data-stu-id="23e06-149">T</span></span><br/> <span data-ttu-id="23e06-150">TITLE</span><span class="sxs-lookup"><span data-stu-id="23e06-150">TITLE</span></span><br/>     | <span data-ttu-id="23e06-151">\_título XCN OID \_</span><span class="sxs-lookup"><span data-stu-id="23e06-151">XCN\_OID\_TITLE</span></span><br/>                      | <span data-ttu-id="23e06-152">Contiene el título de una persona de la organización.</span><span class="sxs-lookup"><span data-stu-id="23e06-152">Contains the title of a person in the organization.</span></span><br/>                                     |



 

<span data-ttu-id="23e06-153">Al inicializar un objeto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , puede identificar el formato del nombre distintivo especificando un valor del tipo de enumeración [**X500NameFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) .</span><span class="sxs-lookup"><span data-stu-id="23e06-153">When you initialize an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object, you can identify the format of the distinguished name by specifying a value from the [**X500NameFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) enumeration type.</span></span> <span data-ttu-id="23e06-154">Por ejemplo, supongamos que el nombre distintivo del sujeto consta del siguiente RDN:</span><span class="sxs-lookup"><span data-stu-id="23e06-154">For example, assume that the subject distinguished name consists of the following RDNs:</span></span><dl> <span data-ttu-id="23e06-155">CN = administrador</span><span class="sxs-lookup"><span data-stu-id="23e06-155">CN=Administrator</span></span>  
<span data-ttu-id="23e06-156">CN = usuarios</span><span class="sxs-lookup"><span data-stu-id="23e06-156">CN=Users</span></span>  
<span data-ttu-id="23e06-157">DC = jdomcsc</span><span class="sxs-lookup"><span data-stu-id="23e06-157">DC=jdomcsc</span></span>  
<span data-ttu-id="23e06-158">DC = nttest</span><span class="sxs-lookup"><span data-stu-id="23e06-158">DC=nttest</span></span>  
<span data-ttu-id="23e06-159">DC = Microsoft</span><span class="sxs-lookup"><span data-stu-id="23e06-159">DC=microsoft</span></span>  
<span data-ttu-id="23e06-160">DC = com</span><span class="sxs-lookup"><span data-stu-id="23e06-160">DC=com</span></span>  
</dl>

<span data-ttu-id="23e06-161">Si concatena estos RDN en la siguiente cadena de nombres distintivos delimitados por comas, puede especificar el valor de **\_ \_ \_ \_ \_ marcador de coma Str del nombre de certificado XCN** al inicializar un objeto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) .</span><span class="sxs-lookup"><span data-stu-id="23e06-161">If you concatenate these RDNs into the following comma-delimited distinguished name string, you can specify the **XCN\_CERT\_NAME\_STR\_COMMA\_FLAG** value when initializing an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object.</span></span>

``` syntax
CN=Administrator,CN=Users,DC=jdomcsc,DC=nttest,DC=microsoft,DC=com
```

## <a name="related-topics"></a><span data-ttu-id="23e06-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23e06-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23e06-163">Codificar un nombre de sujeto</span><span class="sxs-lookup"><span data-stu-id="23e06-163">Encoding a Subject Name</span></span>](encoding-a-subject-name.md)
</dt> <dt>

[<span data-ttu-id="23e06-164">Nombres de sujeto</span><span class="sxs-lookup"><span data-stu-id="23e06-164">Subject Names</span></span>](subject-names.md)
</dt> </dl>

 

 




