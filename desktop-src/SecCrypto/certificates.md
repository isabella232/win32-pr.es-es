---
description: 'Objeto Certificates: representa una colección de objetos Certificate.'
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
ms.openlocfilehash: 8efb9221f39b8544eabe8f6c00d21f6cfdf20c14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098393"
---
# <a name="certificates-object"></a><span data-ttu-id="1c4d5-103">Objeto Certificates</span><span class="sxs-lookup"><span data-stu-id="1c4d5-103">Certificates object</span></span>

<span data-ttu-id="1c4d5-104">\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="1c4d5-105">En su lugar, use [**la clase X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]</span><span class="sxs-lookup"><span data-stu-id="1c4d5-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="1c4d5-106">El **objeto Certificates** representa una colección de [**objetos Certificate.**](certificate.md)</span><span class="sxs-lookup"><span data-stu-id="1c4d5-106">The **Certificates** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="1c4d5-107">Cada [**objeto Certificate**](certificate.md) representa un único certificado [*digital.*](../secgloss/d-gly.md)</span><span class="sxs-lookup"><span data-stu-id="1c4d5-107">Each [**Certificate**](certificate.md) object represents a single [*digital certificate*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="1c4d5-108">El **objeto Certificates** expone las interfaces siguientes:</span><span class="sxs-lookup"><span data-stu-id="1c4d5-108">The **Certificates** object exposes the following interfaces:</span></span>

-   <span data-ttu-id="1c4d5-109">**ICertificates2:** se introdujo en CAPICOM 2.0.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-109">**ICertificates2**: Introduced in CAPICOM 2.0.</span></span>
-   <span data-ttu-id="1c4d5-110">**ICertificates:** se introdujo en CAPICOM 1.0.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-110">**ICertificates**: Introduced in CAPICOM 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="1c4d5-111">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="1c4d5-111">When to use</span></span>

<span data-ttu-id="1c4d5-112">El **objeto Certificates** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="1c4d5-112">The **Certificates** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="1c4d5-113">Agregue o quite un [**objeto Certificate**](certificate.md) a o desde la colección.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-113">Add or remove a [**Certificate**](certificate.md) object to or from the collection.</span></span>
-   <span data-ttu-id="1c4d5-114">Genere un subconjunto de la colección buscando un conjunto de certificados o mostrando un cuadro de diálogo para seleccionar los certificados.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-114">Generate a subset of the collection by finding a set of certificates or by displaying a dialog box to select the certificates.</span></span>
-   <span data-ttu-id="1c4d5-115">Borre todos los [**objetos Certificate**](certificate.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-115">Clear all the [**Certificate**](certificate.md) objects from the collection.</span></span>
-   <span data-ttu-id="1c4d5-116">Recupere el número de certificados de la colección.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-116">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="1c4d5-117">Recupere un objeto [**Certificate**](certificate.md) específico de la colección.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-117">Retrieve a specific [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="1c4d5-118">Recorrer en iteración la colección.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-118">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="1c4d5-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="1c4d5-119">Members</span></span>

<span data-ttu-id="1c4d5-120">El **objeto Certificates** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1c4d5-120">The **Certificates** object has these types of members:</span></span>

-   [<span data-ttu-id="1c4d5-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c4d5-121">Methods</span></span>](#methods)
-   [<span data-ttu-id="1c4d5-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1c4d5-122">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1c4d5-123">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c4d5-123">Methods</span></span>

<span data-ttu-id="1c4d5-124">El **objeto Certificates** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-124">The **Certificates** object has these methods.</span></span>



| <span data-ttu-id="1c4d5-125">Método</span><span class="sxs-lookup"><span data-stu-id="1c4d5-125">Method</span></span>                                | <span data-ttu-id="1c4d5-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c4d5-126">Description</span></span>                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c4d5-127">**Añadir**</span><span class="sxs-lookup"><span data-stu-id="1c4d5-127">**Add**</span></span>](certificates-add.md)       | <span data-ttu-id="1c4d5-128">Agrega un [**objeto Certificate**](certificate.md) a la colección.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-128">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/> <span data-ttu-id="1c4d5-129">(Se hereda de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="1c4d5-129">(Inherited from **CertificatesICertificates2**)</span></span>                                        |
| [<span data-ttu-id="1c4d5-130">**Borrar**</span><span class="sxs-lookup"><span data-stu-id="1c4d5-130">**Clear**</span></span>](certificates-clear.md)   | <span data-ttu-id="1c4d5-131">Quita todos los [**objetos Certificate**](certificate.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-131">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> <span data-ttu-id="1c4d5-132">(Se hereda de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="1c4d5-132">(Inherited from **CertificatesICertificates2**)</span></span>                                |
| [<span data-ttu-id="1c4d5-133">**Buscar**</span><span class="sxs-lookup"><span data-stu-id="1c4d5-133">**Find**</span></span>](certificates-find.md)     | <span data-ttu-id="1c4d5-134">Devuelve un **objeto Certificates** que contiene todos los certificados que coinciden con los criterios de búsqueda especificados.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-134">Returns a **Certificates** object that contains all certificates that match the specified search criteria.</span></span><br/> <span data-ttu-id="1c4d5-135">(Se hereda de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="1c4d5-135">(Inherited from **CertificatesICertificates2**)</span></span> |
| [<span data-ttu-id="1c4d5-136">**Quitar**</span><span class="sxs-lookup"><span data-stu-id="1c4d5-136">**Remove**</span></span>](certificates-remove.md) | <span data-ttu-id="1c4d5-137">Quita un único [**objeto Certificate**](certificate.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-137">Removes a single [**Certificate**](certificate.md) object from the collection.</span></span><br/> <span data-ttu-id="1c4d5-138">(Se hereda de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="1c4d5-138">(Inherited from **CertificatesICertificates2**)</span></span>                            |
| [<span data-ttu-id="1c4d5-139">**Guardar**</span><span class="sxs-lookup"><span data-stu-id="1c4d5-139">**Save**</span></span>](certificates-save.md)     | <span data-ttu-id="1c4d5-140">Guarda los certificados en un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-140">Saves the certificates to a specified file.</span></span><br/> <span data-ttu-id="1c4d5-141">(Se hereda de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="1c4d5-141">(Inherited from **CertificatesICertificates2**)</span></span>                                                                |
| [<span data-ttu-id="1c4d5-142">**Seleccionar**</span><span class="sxs-lookup"><span data-stu-id="1c4d5-142">**Select**</span></span>](certificates-select.md) | <span data-ttu-id="1c4d5-143">Muestra un cuadro de diálogo para seleccionar certificados y devuelve una colección de esos certificados seleccionados.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-143">Displays a dialog box for selecting certificates and returns a collection of those certificates selected.</span></span><br/> <span data-ttu-id="1c4d5-144">(Se hereda de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="1c4d5-144">(Inherited from **CertificatesICertificates2**)</span></span>  |



 

### <a name="properties"></a><span data-ttu-id="1c4d5-145">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1c4d5-145">Properties</span></span>

<span data-ttu-id="1c4d5-146">El **objeto Certificates** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-146">The **Certificates** object has these properties.</span></span>



| <span data-ttu-id="1c4d5-147">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1c4d5-147">Property</span></span>                                             | <span data-ttu-id="1c4d5-148">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="1c4d5-148">Access type</span></span>          | <span data-ttu-id="1c4d5-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c4d5-149">Description</span></span>                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c4d5-150">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="1c4d5-150">**\_NewEnum**</span></span>](certificates-newenum.md)<br/> | <span data-ttu-id="1c4d5-151">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1c4d5-151">Read-only</span></span><br/> | <span data-ttu-id="1c4d5-152">Recupera una [**interfaz IEnumVARIANT en**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un objeto que se puede usar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-152">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="1c4d5-153">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="1c4d5-153">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="1c4d5-154">**Contar**</span><span class="sxs-lookup"><span data-stu-id="1c4d5-154">**Count**</span></span>](certificates-count.md)<br/>       | <span data-ttu-id="1c4d5-155">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1c4d5-155">Read-only</span></span><br/> | <span data-ttu-id="1c4d5-156">Recupera el número de [**objetos Certificate**](certificate.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-156">Retrieves the number of [**Certificate**](certificate.md) objects in the collection.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="1c4d5-157">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1c4d5-157">**Item**</span></span>](certificates-item.md)<br/>         | <span data-ttu-id="1c4d5-158">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1c4d5-158">Read-only</span></span><br/> | <span data-ttu-id="1c4d5-159">Recupera un [**objeto Certificate**](certificate.md) que representa el certificado indexado de la colección.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-159">Retrieves a [**Certificate**](certificate.md) object that represents the indexed certificate of the collection.</span></span> <span data-ttu-id="1c4d5-160">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-160">This is the default property.</span></span><br/> <span data-ttu-id="1c4d5-161">(Se hereda de **CertificatesICertificates2ICertificates**)</span><span class="sxs-lookup"><span data-stu-id="1c4d5-161">(Inherited from **CertificatesICertificates2ICertificates**)</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="1c4d5-162">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1c4d5-162">Remarks</span></span>

<span data-ttu-id="1c4d5-163">Se puede crear el objeto **Certificates** y es seguro para el scripting.</span><span class="sxs-lookup"><span data-stu-id="1c4d5-163">The **Certificates** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="1c4d5-164">El ProgID del **objeto Certificates** es "CAPICOM. Certificates.2".</span><span class="sxs-lookup"><span data-stu-id="1c4d5-164">The ProgID for the **Certificates** object is "CAPICOM.Certificates.2".</span></span>

<span data-ttu-id="1c4d5-165">**CAPICOM 1. *x:*** el ProgID del **objeto Certificates** es "CAPICOM. Certificates.1".</span><span class="sxs-lookup"><span data-stu-id="1c4d5-165">**CAPICOM 1.*x*:** The ProgID for the **Certificates** object is "CAPICOM.Certificates.1".</span></span>

## <a name="requirements"></a><span data-ttu-id="1c4d5-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c4d5-166">Requirements</span></span>



| <span data-ttu-id="1c4d5-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c4d5-167">Requirement</span></span> | <span data-ttu-id="1c4d5-168">Valor</span><span class="sxs-lookup"><span data-stu-id="1c4d5-168">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c4d5-169">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="1c4d5-169">End of client support</span></span><br/> | <span data-ttu-id="1c4d5-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c4d5-170">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1c4d5-171">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="1c4d5-171">End of server support</span></span><br/> | <span data-ttu-id="1c4d5-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c4d5-172">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1c4d5-173">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="1c4d5-173">Redistributable</span></span><br/>       | <span data-ttu-id="1c4d5-174">CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c4d5-174">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1c4d5-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1c4d5-175">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1c4d5-176"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c4d5-176"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c4d5-177">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1c4d5-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c4d5-178">**Objetos criptografía**</span><span class="sxs-lookup"><span data-stu-id="1c4d5-178">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
