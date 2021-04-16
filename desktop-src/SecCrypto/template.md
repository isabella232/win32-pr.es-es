---
description: Representa la plantilla de extensión de certificado del certificado.
ms.assetid: 1ae9220a-f6b3-47c5-bd08-a36ffd84e1f9
title: Objeto de plantilla
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fedd64979ad74ceac3f6d54af58c57d8d8b2b134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649974"
---
# <a name="template-object"></a><span data-ttu-id="55e2f-103">Objeto de plantilla</span><span class="sxs-lookup"><span data-stu-id="55e2f-103">Template object</span></span>

<span data-ttu-id="55e2f-104">\[El objeto de **plantilla** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="55e2f-104">\[The **Template** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="55e2f-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID de la plantilla de certificado para recuperar la plantilla de extensión de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="55e2f-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="55e2f-106">El objeto de **plantilla** representa la plantilla de extensión de certificado del certificado.</span><span class="sxs-lookup"><span data-stu-id="55e2f-106">The **Template** object represents the certificate extension template of the certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="55e2f-107">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="55e2f-107">When to use</span></span>

<span data-ttu-id="55e2f-108">El objeto de **plantilla** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="55e2f-108">The **Template** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="55e2f-109">Determine si la plantilla está marcada como crítica o presente.</span><span class="sxs-lookup"><span data-stu-id="55e2f-109">Determine whether the template is marked critical or present.</span></span>
-   <span data-ttu-id="55e2f-110">Recupere el [*identificador de objeto*](../secgloss/o-gly.md) (OID) o el nombre de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="55e2f-110">Retrieve the [*object identifier*](../secgloss/o-gly.md) (OID) or name of the template.</span></span>
-   <span data-ttu-id="55e2f-111">Recupere la versión secundaria o principal de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="55e2f-111">Retrieve the minor or major version of the template.</span></span>

## <a name="members"></a><span data-ttu-id="55e2f-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="55e2f-112">Members</span></span>

<span data-ttu-id="55e2f-113">El objeto de **plantilla** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="55e2f-113">The **Template** object has these types of members:</span></span>

-   [<span data-ttu-id="55e2f-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="55e2f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55e2f-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="55e2f-115">Properties</span></span>

<span data-ttu-id="55e2f-116">El objeto de **plantilla** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="55e2f-116">The **Template** object has these properties.</span></span>



| <span data-ttu-id="55e2f-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="55e2f-117">Property</span></span>                                                 | <span data-ttu-id="55e2f-118">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="55e2f-118">Access type</span></span>          | <span data-ttu-id="55e2f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="55e2f-119">Description</span></span>                                                                                            |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55e2f-120">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="55e2f-120">**IsCritical**</span></span>](template-iscritical.md)<br/>     | <span data-ttu-id="55e2f-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="55e2f-121">Read-only</span></span><br/> | <span data-ttu-id="55e2f-122">Recupera un valor booleano que indica si la extensión de plantilla está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="55e2f-122">Retrieves a Boolean value that indicates whether the template extension is marked critical.</span></span><br/> |
| [<span data-ttu-id="55e2f-123">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="55e2f-123">**IsPresent**</span></span>](template-ispresent.md)<br/>       | <span data-ttu-id="55e2f-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="55e2f-124">Read-only</span></span><br/> | <span data-ttu-id="55e2f-125">Recupera un valor booleano que indica si la extensión de plantilla está presente.</span><span class="sxs-lookup"><span data-stu-id="55e2f-125">Retrieves a Boolean value that indicates whether the template extension is present.</span></span><br/>         |
| [<span data-ttu-id="55e2f-126">**MajorVersion**</span><span class="sxs-lookup"><span data-stu-id="55e2f-126">**MajorVersion**</span></span>](template-majorversion.md)<br/> | <span data-ttu-id="55e2f-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="55e2f-127">Read-only</span></span><br/> | <span data-ttu-id="55e2f-128">Recupera el número de versión principal de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="55e2f-128">Retrieves the major version number of the template.</span></span><br/>                                         |
| [<span data-ttu-id="55e2f-129">**MinorVersion**</span><span class="sxs-lookup"><span data-stu-id="55e2f-129">**MinorVersion**</span></span>](template-minorversion.md)<br/> | <span data-ttu-id="55e2f-130">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="55e2f-130">Read-only</span></span><br/> | <span data-ttu-id="55e2f-131">Recupera el número de versión secundaria de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="55e2f-131">Retrieves the minor version number of the template.</span></span><br/>                                         |
| [<span data-ttu-id="55e2f-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="55e2f-132">**Name**</span></span>](template-name.md)<br/>                 | <span data-ttu-id="55e2f-133">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="55e2f-133">Read-only</span></span><br/> | <span data-ttu-id="55e2f-134">Recupera una cadena que contiene el nombre de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="55e2f-134">Retrieves a string that contains the name of the template.</span></span><br/>                                  |
| [<span data-ttu-id="55e2f-135">**OID**</span><span class="sxs-lookup"><span data-stu-id="55e2f-135">**OID**</span></span>](template-oid.md)<br/>                   | <span data-ttu-id="55e2f-136">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="55e2f-136">Read-only</span></span><br/> | <span data-ttu-id="55e2f-137">Recupera un objeto [**OID**](oid.md) que identifica el objeto de **plantilla** .</span><span class="sxs-lookup"><span data-stu-id="55e2f-137">Retrieves an [**OID**](oid.md) object that identifies the **Template** object.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="55e2f-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55e2f-138">Remarks</span></span>

<span data-ttu-id="55e2f-139">No se puede crear el objeto de **plantilla** .</span><span class="sxs-lookup"><span data-stu-id="55e2f-139">The **Template** object cannot be created.</span></span>

<span data-ttu-id="55e2f-140">El método [**Certificate. template**](certificate-template.md) devuelve un objeto de **plantilla** .</span><span class="sxs-lookup"><span data-stu-id="55e2f-140">A **Template** object is returned by the [**Certificate.Template**](certificate-template.md) method.</span></span>

<span data-ttu-id="55e2f-141">CAPICOM utiliza dos versiones diferentes de las plantillas de certificado.</span><span class="sxs-lookup"><span data-stu-id="55e2f-141">CAPICOM uses two different versions of certificate templates.</span></span> <span data-ttu-id="55e2f-142">En la tabla siguiente se muestra el nombre y el OID de cada versión de plantilla de certificado.</span><span class="sxs-lookup"><span data-stu-id="55e2f-142">The following table shows the name and OID for each certificate template version.</span></span>



| <span data-ttu-id="55e2f-143">Versión</span><span class="sxs-lookup"><span data-stu-id="55e2f-143">Version</span></span> | <span data-ttu-id="55e2f-144">Nombre</span><span class="sxs-lookup"><span data-stu-id="55e2f-144">Name</span></span>                               | <span data-ttu-id="55e2f-145">OID</span><span class="sxs-lookup"><span data-stu-id="55e2f-145">OID</span></span>                    |
|---------|------------------------------------|------------------------|
| <span data-ttu-id="55e2f-146">V1</span><span class="sxs-lookup"><span data-stu-id="55e2f-146">V1</span></span>      | <span data-ttu-id="55e2f-147">szOID \_ inscribir \_ CERTTYPE \_ extensión</span><span class="sxs-lookup"><span data-stu-id="55e2f-147">szOID\_ENROLL\_CERTTYPE\_EXTENSION</span></span> | <span data-ttu-id="55e2f-148">"1.3.6.1.4.1.311.20.2"</span><span class="sxs-lookup"><span data-stu-id="55e2f-148">"1.3.6.1.4.1.311.20.2"</span></span> |
| <span data-ttu-id="55e2f-149">V2</span><span class="sxs-lookup"><span data-stu-id="55e2f-149">V2</span></span>      | <span data-ttu-id="55e2f-150">\_plantilla de certificado de szOID \_</span><span class="sxs-lookup"><span data-stu-id="55e2f-150">szOID\_CERTIFICATE\_TEMPLATE</span></span>       | <span data-ttu-id="55e2f-151">"1.3.6.1.4.1.311.21.7"</span><span class="sxs-lookup"><span data-stu-id="55e2f-151">"1.3.6.1.4.1.311.21.7"</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="55e2f-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55e2f-152">Requirements</span></span>



| <span data-ttu-id="55e2f-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="55e2f-153">Requirement</span></span> | <span data-ttu-id="55e2f-154">Value</span><span class="sxs-lookup"><span data-stu-id="55e2f-154">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55e2f-155">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="55e2f-155">Redistributable</span></span><br/> | <span data-ttu-id="55e2f-156">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="55e2f-156">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="55e2f-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="55e2f-157">DLL</span></span><br/>             | <dl> <span data-ttu-id="55e2f-158"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55e2f-158"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
