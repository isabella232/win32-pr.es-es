---
description: Representa una colección de objetos de certificado.
ms.assetid: 82011c49-38fb-4261-8fb3-b76859da8a9e
title: Objeto Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e8c12c16820342c5687720a35ce81aa7b94f180
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670303"
---
# <a name="certificates-object"></a><span data-ttu-id="a8cf0-103">Objeto Certificates</span><span class="sxs-lookup"><span data-stu-id="a8cf0-103">Certificates object</span></span>

<span data-ttu-id="a8cf0-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a8cf0-105">En su lugar, use la [**clase X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a8cf0-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a8cf0-106">El objeto de **certificados** representa una colección de objetos de [**certificado**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="a8cf0-106">The **Certificates** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="a8cf0-107">Cada objeto de [**certificado**](certificate.md) representa un único [*certificado digital*](../secgloss/d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a8cf0-107">Each [**Certificate**](certificate.md) object represents a single [*digital certificate*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="a8cf0-108">El objeto **Certificates** expone las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="a8cf0-108">The **Certificates** object exposes the following interfaces:</span></span>

-   <span data-ttu-id="a8cf0-109">**ICertificates2**: introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-109">**ICertificates2**: Introduced in CAPICOM 2.0.</span></span>
-   <span data-ttu-id="a8cf0-110">**ICertificates**: introducido en CAPICOM 1,0.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-110">**ICertificates**: Introduced in CAPICOM 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="a8cf0-111">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="a8cf0-111">When to use</span></span>

<span data-ttu-id="a8cf0-112">El objeto de **certificados** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="a8cf0-112">The **Certificates** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="a8cf0-113">Agregue o quite un objeto de [**certificado**](certificate.md) de o de la colección.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-113">Add or remove a [**Certificate**](certificate.md) object to or from the collection.</span></span>
-   <span data-ttu-id="a8cf0-114">Genere un subconjunto de la colección buscando un conjunto de certificados o mostrando un cuadro de diálogo para seleccionar los certificados.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-114">Generate a subset of the collection by finding a set of certificates or by displaying a dialog box to select the certificates.</span></span>
-   <span data-ttu-id="a8cf0-115">Borre todos los objetos de [**certificado**](certificate.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-115">Clear all the [**Certificate**](certificate.md) objects from the collection.</span></span>
-   <span data-ttu-id="a8cf0-116">Recupere el número de certificados de la colección.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-116">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="a8cf0-117">Recupera un objeto de [**certificado**](certificate.md) específico de la colección.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-117">Retrieve a specific [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="a8cf0-118">Recorrer en iteración la colección.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-118">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="a8cf0-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="a8cf0-119">Members</span></span>

<span data-ttu-id="a8cf0-120">El objeto de **certificados** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a8cf0-120">The **Certificates** object has these types of members:</span></span>

-   [<span data-ttu-id="a8cf0-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="a8cf0-121">Methods</span></span>](#methods)
-   [<span data-ttu-id="a8cf0-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a8cf0-122">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a8cf0-123">Métodos</span><span class="sxs-lookup"><span data-stu-id="a8cf0-123">Methods</span></span>

<span data-ttu-id="a8cf0-124">El objeto de **certificados** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-124">The **Certificates** object has these methods.</span></span>



| <span data-ttu-id="a8cf0-125">Método</span><span class="sxs-lookup"><span data-stu-id="a8cf0-125">Method</span></span>                                | <span data-ttu-id="a8cf0-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8cf0-126">Description</span></span>                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8cf0-127">**Agréguela**</span><span class="sxs-lookup"><span data-stu-id="a8cf0-127">**Add**</span></span>](certificates-add.md)       | <span data-ttu-id="a8cf0-128">Agrega un objeto de [**certificado**](certificate.md) a la colección.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-128">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/> <span data-ttu-id="a8cf0-129">(Se hereda de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="a8cf0-129">(Inherited from **CertificatesICertificates2**)</span></span>                                        |
| [<span data-ttu-id="a8cf0-130">**Claridad**</span><span class="sxs-lookup"><span data-stu-id="a8cf0-130">**Clear**</span></span>](certificates-clear.md)   | <span data-ttu-id="a8cf0-131">Quita todos los objetos de [**certificado**](certificate.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-131">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> <span data-ttu-id="a8cf0-132">(Se hereda de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="a8cf0-132">(Inherited from **CertificatesICertificates2**)</span></span>                                |
| [<span data-ttu-id="a8cf0-133">**Buscar**</span><span class="sxs-lookup"><span data-stu-id="a8cf0-133">**Find**</span></span>](certificates-find.md)     | <span data-ttu-id="a8cf0-134">Devuelve un objeto de **certificados** que contiene todos los certificados que coinciden con los criterios de búsqueda especificados.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-134">Returns a **Certificates** object that contains all certificates that match the specified search criteria.</span></span><br/> <span data-ttu-id="a8cf0-135">(Se hereda de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="a8cf0-135">(Inherited from **CertificatesICertificates2**)</span></span> |
| [<span data-ttu-id="a8cf0-136">**Retirar**</span><span class="sxs-lookup"><span data-stu-id="a8cf0-136">**Remove**</span></span>](certificates-remove.md) | <span data-ttu-id="a8cf0-137">Quita un objeto de [**certificado**](certificate.md) único de la colección.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-137">Removes a single [**Certificate**](certificate.md) object from the collection.</span></span><br/> <span data-ttu-id="a8cf0-138">(Se hereda de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="a8cf0-138">(Inherited from **CertificatesICertificates2**)</span></span>                            |
| [<span data-ttu-id="a8cf0-139">**Guardar**</span><span class="sxs-lookup"><span data-stu-id="a8cf0-139">**Save**</span></span>](certificates-save.md)     | <span data-ttu-id="a8cf0-140">Guarda los certificados en un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-140">Saves the certificates to a specified file.</span></span><br/> <span data-ttu-id="a8cf0-141">(Se hereda de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="a8cf0-141">(Inherited from **CertificatesICertificates2**)</span></span>                                                                |
| [<span data-ttu-id="a8cf0-142">**Seleccionar**</span><span class="sxs-lookup"><span data-stu-id="a8cf0-142">**Select**</span></span>](certificates-select.md) | <span data-ttu-id="a8cf0-143">Muestra un cuadro de diálogo para seleccionar certificados y devuelve una colección de los certificados seleccionados.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-143">Displays a dialog box for selecting certificates and returns a collection of those certificates selected.</span></span><br/> <span data-ttu-id="a8cf0-144">(Se hereda de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="a8cf0-144">(Inherited from **CertificatesICertificates2**)</span></span>  |



 

### <a name="properties"></a><span data-ttu-id="a8cf0-145">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a8cf0-145">Properties</span></span>

<span data-ttu-id="a8cf0-146">El objeto de **certificados** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-146">The **Certificates** object has these properties.</span></span>



| <span data-ttu-id="a8cf0-147">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a8cf0-147">Property</span></span>                                             | <span data-ttu-id="a8cf0-148">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="a8cf0-148">Access type</span></span>          | <span data-ttu-id="a8cf0-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8cf0-149">Description</span></span>                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8cf0-150">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="a8cf0-150">**\_NewEnum**</span></span>](certificates-newenum.md)<br/> | <span data-ttu-id="a8cf0-151">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a8cf0-151">Read-only</span></span><br/> | <span data-ttu-id="a8cf0-152">Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-152">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="a8cf0-153">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="a8cf0-153">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="a8cf0-154">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="a8cf0-154">**Count**</span></span>](certificates-count.md)<br/>       | <span data-ttu-id="a8cf0-155">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a8cf0-155">Read-only</span></span><br/> | <span data-ttu-id="a8cf0-156">Recupera el número de objetos de [**certificado**](certificate.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-156">Retrieves the number of [**Certificate**](certificate.md) objects in the collection.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="a8cf0-157">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a8cf0-157">**Item**</span></span>](certificates-item.md)<br/>         | <span data-ttu-id="a8cf0-158">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a8cf0-158">Read-only</span></span><br/> | <span data-ttu-id="a8cf0-159">Recupera un objeto de [**certificado**](certificate.md) que representa el certificado indizado de la colección.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-159">Retrieves a [**Certificate**](certificate.md) object that represents the indexed certificate of the collection.</span></span> <span data-ttu-id="a8cf0-160">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-160">This is the default property.</span></span><br/> <span data-ttu-id="a8cf0-161">(Se hereda de **CertificatesICertificates2ICertificates**)</span><span class="sxs-lookup"><span data-stu-id="a8cf0-161">(Inherited from **CertificatesICertificates2ICertificates**)</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="a8cf0-162">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8cf0-162">Remarks</span></span>

<span data-ttu-id="a8cf0-163">Se puede crear el objeto de **certificados** y es seguro para el scripting.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-163">The **Certificates** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="a8cf0-164">El ProgID del objeto de **certificados** es "CAPICOM. Certificates. 2 ".</span><span class="sxs-lookup"><span data-stu-id="a8cf0-164">The ProgID for the **Certificates** object is "CAPICOM.Certificates.2".</span></span>

<span data-ttu-id="a8cf0-165">**CAPICOM 1. *x*:** el identificador de programa (ProgID) del objeto de **certificados** es "CAPICOM. Certificates. 1 ".</span><span class="sxs-lookup"><span data-stu-id="a8cf0-165">**CAPICOM 1.*x*:** The ProgID for the **Certificates** object is "CAPICOM.Certificates.1".</span></span>

## <a name="requirements"></a><span data-ttu-id="a8cf0-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8cf0-166">Requirements</span></span>



| <span data-ttu-id="a8cf0-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8cf0-167">Requirement</span></span> | <span data-ttu-id="a8cf0-168">Value</span><span class="sxs-lookup"><span data-stu-id="a8cf0-168">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8cf0-169">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a8cf0-169">End of client support</span></span><br/> | <span data-ttu-id="a8cf0-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8cf0-170">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a8cf0-171">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="a8cf0-171">End of server support</span></span><br/> | <span data-ttu-id="a8cf0-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8cf0-172">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a8cf0-173">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="a8cf0-173">Redistributable</span></span><br/>       | <span data-ttu-id="a8cf0-174">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="a8cf0-174">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a8cf0-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a8cf0-175">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a8cf0-176"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8cf0-176"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8cf0-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8cf0-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8cf0-178">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="a8cf0-178">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
