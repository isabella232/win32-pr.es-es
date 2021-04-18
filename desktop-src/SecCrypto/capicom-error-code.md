---
description: Define los códigos de error devueltos por CAPICOM.
ms.assetid: e72b8290-b482-4629-8b87-5a15677865a6
title: Enumeración CAPICOM_ERROR_CODE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ERROR_CODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: ccd4963c83f1ad7ce3bc686b7736ce47d699ce30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671044"
---
# <a name="capicom_error_code-enumeration"></a><span data-ttu-id="e5d2e-103">\_Enumeración de códigos de error de CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="e5d2e-103">CAPICOM\_ERROR\_CODE enumeration</span></span>

<span data-ttu-id="e5d2e-104">El tipo de enumeración del **\_ \_ código de error CAPICOM** define los códigos de error devueltos por CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-104">The **CAPICOM\_ERROR\_CODE** enumeration type defines error codes that are returned by CAPICOM.</span></span>

> [!Note]  
> <span data-ttu-id="e5d2e-105">Los errores de Visual Basic Scripting Edition devuelven un valor de **Err. Number** mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-105">Visual Basic Scripting Edition errors return an **Err.number** value greater than zero.</span></span> <span data-ttu-id="e5d2e-106">Para esos errores, los valores de **Err. Description** proporcionan información sobre la causa del error.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-106">For those errors, **Err.Description** values provide information about the cause of the error.</span></span> <span data-ttu-id="e5d2e-107">Además de Visual Basic Scripting Edition errores, los errores de CAPICOM devuelven los códigos definidos por el **\_ \_ código de error de CAPICOM**.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-107">In addition to Visual Basic Scripting Edition errors, CAPICOM errors return the codes defined by **CAPICOM\_ERROR\_CODE**.</span></span>

 

## <a name="members"></a><span data-ttu-id="e5d2e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e5d2e-108">Members</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5d2e-109">Miembro</span><span class="sxs-lookup"><span data-stu-id="e5d2e-109">Member</span></span></th>
<th><span data-ttu-id="e5d2e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5d2e-110">Description</span></span></th>
<th><span data-ttu-id="e5d2e-111">Value</span><span class="sxs-lookup"><span data-stu-id="e5d2e-111">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5d2e-112"><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-112"><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="e5d2e-113">Se usó un tipo de codificación que no es válido.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-113">An encoding type that is not valid was used.</span></span><br/> <span data-ttu-id="e5d2e-114">En la lista siguiente se muestran los tipos de codificación válidos:</span><span class="sxs-lookup"><span data-stu-id="e5d2e-114">The following list shows the valid encoding types:</span></span>
<ul>
<li><span data-ttu-id="e5d2e-115">CAPICOM_ENCODE_ANY</span><span class="sxs-lookup"><span data-stu-id="e5d2e-115">CAPICOM_ENCODE_ANY</span></span></li>
<li><span data-ttu-id="e5d2e-116">CAPICOM_ENCODE_BASE64</span><span class="sxs-lookup"><span data-stu-id="e5d2e-116">CAPICOM_ENCODE_BASE64</span></span></li>
<li><span data-ttu-id="e5d2e-117">CAPICOM_ENCODE_BINARY</span><span class="sxs-lookup"><span data-stu-id="e5d2e-117">CAPICOM_ENCODE_BINARY</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="e5d2e-118">0x80880100</span><span class="sxs-lookup"><span data-stu-id="e5d2e-118">0x80880100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-119"><strong>CAPICOM_E_EKU_INVALID_OID</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-119"><strong>CAPICOM_E_EKU_INVALID_OID</strong></span></span></td>
<td><span data-ttu-id="e5d2e-120">No se puede establecer la propiedad <a href="eku-oid.md"><strong>OID</strong></a> del objeto <a href="eku.md"><strong>EKU</strong></a> porque la propiedad <a href="eku-name.md"><strong>Name</strong></a> no está establecida en CAPICOM_EKU_OTHER.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-120">The <a href="eku-oid.md"><strong>OID</strong></a> property of the <a href="eku.md"><strong>EKU</strong></a> object cannot be set because the <a href="eku-name.md"><strong>Name</strong></a> property is not set to CAPICOM_EKU_OTHER.</span></span><br/> <span data-ttu-id="e5d2e-121">Establezca la propiedad <a href="eku-name.md"><strong>Name</strong></a> en CAPICOM_EKU_OTHER antes de establecer la propiedad <a href="eku-oid.md"><strong>OID</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-121">Set the <a href="eku-name.md"><strong>Name</strong></a> property to CAPICOM_EKU_OTHER before setting the <a href="eku-oid.md"><strong>OID</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-122">0x80880200</span><span class="sxs-lookup"><span data-stu-id="e5d2e-122">0x80880200</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-123"><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-123"><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-124">No se ha inicializado la propiedad <a href="eku-oid.md"><strong>OID</strong></a> del objeto <a href="eku.md"><strong>EKU</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-124">The <a href="eku-oid.md"><strong>OID</strong></a> property of the <a href="eku.md"><strong>EKU</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="e5d2e-125">Establezca la propiedad <a href="eku-name.md"><strong>Name</strong></a> en algo distinto de CAPICOM_EKU_OTHER, o bien establezca la propiedad <strong>Name</strong> en CAPICOM_EKU_OTHER y la propiedad <a href="eku-oid.md"><strong>OID</strong></a> en un valor.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-125">Either set the <a href="eku-name.md"><strong>Name</strong></a> property to anything other than CAPICOM_EKU_OTHER, or set the <strong>Name</strong> property to CAPICOM_EKU_OTHER and the <a href="eku-oid.md"><strong>OID</strong></a> property to a value.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-126">0x80880201</span><span class="sxs-lookup"><span data-stu-id="e5d2e-126">0x80880201</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-127"><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-127"><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-128">No se ha inicializado el objeto de <a href="certificate.md"><strong>certificado</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-128">The <a href="certificate.md"><strong>Certificate</strong></a> object has not been initialized.</span></span><br/> <span data-ttu-id="e5d2e-129">Normalmente, este código de error se devuelve cuando se crea una instancia de un objeto de <a href="certificate.md"><strong>certificado</strong></a> pero no se asocia a un certificado digital.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-129">Usually, this error code is returned when a <a href="certificate.md"><strong>Certificate</strong></a> object is instantiated but not associated with a digital certificate.</span></span> <span data-ttu-id="e5d2e-130">Para asociar el objeto a un certificado digital, asígnelo a un objeto de <strong>certificado</strong> existente o llame al método de <a href="certificate-import.md"><strong>importación</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-130">To associate the object with a digital certificate, either assign it to an existing <strong>Certificate</strong> object or call the <a href="certificate-import.md"><strong>Import</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-131">0x80880210</span><span class="sxs-lookup"><span data-stu-id="e5d2e-131">0x80880210</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-132"><strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-132"><strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong></span></span></td>
<td><span data-ttu-id="e5d2e-133">El objeto de <a href="certificate.md"><strong>certificado</strong></a> no tiene una clave privada asociada.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-133">The <a href="certificate.md"><strong>Certificate</strong></a> object does not have an associated private key.</span></span><br/> <span data-ttu-id="e5d2e-134">Este código de error se devuelve cuando se intenta firmar datos mediante la clave privada del firmante, pero el objeto de <a href="certificate.md"><strong>certificado</strong></a> asociado al objeto de <a href="signer.md"><strong>firmante</strong></a> no se puede usar para la operación de firma.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-134">This error code is returned when an attempt is made to sign data using the signer's private key, but the <a href="certificate.md"><strong>Certificate</strong></a> object that is associated with the <a href="signer.md"><strong>Signer</strong></a> object cannot be used for the signing operation.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-135">0x80880211</span><span class="sxs-lookup"><span data-stu-id="e5d2e-135">0x80880211</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-136"><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-136"><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></span></span></td>
<td><span data-ttu-id="e5d2e-137">No se ha inicializado el objeto de <a href="chain.md"><strong>cadena</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-137">The <a href="chain.md"><strong>Chain</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="e5d2e-138">Para inicializar el objeto de <a href="chain.md"><strong>cadena</strong></a> , llame al método de <a href="chain-build.md"><strong>compilación</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-138">To initialize the <a href="chain.md"><strong>Chain</strong></a> object, call the <a href="chain-build.md"><strong>Build</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-139">0x80880220</span><span class="sxs-lookup"><span data-stu-id="e5d2e-139">0x80880220</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-140"><strong>CAPICOM_E_STORE_NOT_OPENED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-140"><strong>CAPICOM_E_STORE_NOT_OPENED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-141">No se ha inicializado el objeto de <a href="store.md"><strong>almacén</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-141">The <a href="store.md"><strong>Store</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="e5d2e-142">Para inicializar el objeto de <a href="store.md"><strong>almacenamiento</strong></a> , llame al método <a href="store-open.md"><strong>Open</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-142">To initialize the <a href="store.md"><strong>Store</strong></a> object, call the <a href="store-open.md"><strong>Open</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-143">0x80880230</span><span class="sxs-lookup"><span data-stu-id="e5d2e-143">0x80880230</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-144"><strong>CAPICOM_E_STORE_EMPTY</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-144"><strong>CAPICOM_E_STORE_EMPTY</strong></span></span></td>
<td><span data-ttu-id="e5d2e-145">El objeto de <a href="store.md"><strong>almacén</strong></a> no contiene ningún objeto de <a href="certificate.md"><strong>certificado</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-145">The <a href="store.md"><strong>Store</strong></a> object does not contain any <a href="certificate.md"><strong>Certificate</strong></a> objects.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-146">0x80880231</span><span class="sxs-lookup"><span data-stu-id="e5d2e-146">0x80880231</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-147"><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-147"><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></span></span></td>
<td><span data-ttu-id="e5d2e-148">El parámetro <em>OpenMode</em> del método <a href="store-open.md"><strong>Store. Open</strong></a> no contiene un valor válido de CAPICOM_STORE_OPEN_MODE.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-148">The <em>OpenMode</em> parameter of the <a href="store-open.md"><strong>Store.Open</strong></a> method does not contain a valid value of CAPICOM_STORE_OPEN_MODE.</span></span><br/> <span data-ttu-id="e5d2e-149">En la lista siguiente se muestran los valores válidos de CAPICOM_STORE_OPEN_MODE:</span><span class="sxs-lookup"><span data-stu-id="e5d2e-149">The following list shows the valid values of CAPICOM_STORE_OPEN_MODE:</span></span>
<ul>
<li><span data-ttu-id="e5d2e-150">CAPICOM_STORE_OPEN_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="e5d2e-150">CAPICOM_STORE_OPEN_READ_ONLY</span></span></li>
<li><span data-ttu-id="e5d2e-151">CAPICOM_STORE_OPEN_READ_WRITE</span><span class="sxs-lookup"><span data-stu-id="e5d2e-151">CAPICOM_STORE_OPEN_READ_WRITE</span></span></li>
<li><span data-ttu-id="e5d2e-152">CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="e5d2e-152">CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</span></span></li>
<li><span data-ttu-id="e5d2e-153">CAPICOM_STORE_OPEN_EXISTING_ONLY</span><span class="sxs-lookup"><span data-stu-id="e5d2e-153">CAPICOM_STORE_OPEN_EXISTING_ONLY</span></span></li>
<li><span data-ttu-id="e5d2e-154">CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</span><span class="sxs-lookup"><span data-stu-id="e5d2e-154">CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="e5d2e-155">0x80880232</span><span class="sxs-lookup"><span data-stu-id="e5d2e-155">0x80880232</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-156"><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-156"><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></span></span></td>
<td><span data-ttu-id="e5d2e-157">El valor <em>SaveAs</em> pasado al método <a href="store-export.md"><strong>Export</strong></a> del objeto <a href="store.md"><strong>Store</strong></a> no era válido.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-157">The <em>SaveAs</em> value passed to the <a href="store-export.md"><strong>Export</strong></a> method of the <a href="store.md"><strong>Store</strong></a> object was not valid.</span></span> <br/> <span data-ttu-id="e5d2e-158">En la lista siguiente se muestran los valores de <em>SaveAs</em> válidos:</span><span class="sxs-lookup"><span data-stu-id="e5d2e-158">The following list shows the valid <em>SaveAs</em> values:</span></span>
<ul>
<li><span data-ttu-id="e5d2e-159">CAPICOM_STORE_SAVE_AS_SERIALIZED</span><span class="sxs-lookup"><span data-stu-id="e5d2e-159">CAPICOM_STORE_SAVE_AS_SERIALIZED</span></span></li>
<li><span data-ttu-id="e5d2e-160">CAPICOM_STORE_SAVE_AS_PKCS7</span><span class="sxs-lookup"><span data-stu-id="e5d2e-160">CAPICOM_STORE_SAVE_AS_PKCS7</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="e5d2e-161">0x80880233</span><span class="sxs-lookup"><span data-stu-id="e5d2e-161">0x80880233</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-162"><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-162"><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-163">No se ha inicializado la propiedad <a href="attribute-name.md"><strong>Name</strong></a> del objeto de <a href="attribute.md"><strong>atributo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-163">The <a href="attribute-name.md"><strong>Name</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="e5d2e-164">Establezca la propiedad <a href="attribute-name.md"><strong>nombre</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-164">Set the <a href="attribute-name.md"><strong>Name</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-165">0x80880240</span><span class="sxs-lookup"><span data-stu-id="e5d2e-165">0x80880240</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-166"><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-166"><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-167">No se ha inicializado la propiedad <a href="attribute-value.md"><strong>Value</strong></a> del objeto de <a href="attribute.md"><strong>atributo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-167">The <a href="attribute-value.md"><strong>Value</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="e5d2e-168">Establezca la propiedad <a href="attribute-value.md"><strong>Value</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-168">Set the <a href="attribute-value.md"><strong>Value</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-169">0x80880241</span><span class="sxs-lookup"><span data-stu-id="e5d2e-169">0x80880241</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-170"><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-170"><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></span></span></td>
<td><span data-ttu-id="e5d2e-171">La propiedad de <a href="attribute-name.md"><strong>nombre</strong></a> del objeto de <a href="attribute.md"><strong>atributo</strong></a> no es válida.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-171">The <a href="attribute-name.md"><strong>Name</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="e5d2e-172">En la lista siguiente se muestran los nombres de atributo válidos:</span><span class="sxs-lookup"><span data-stu-id="e5d2e-172">The following list shows the valid attribute names:</span></span>
<ul>
<li><span data-ttu-id="e5d2e-173">CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</span><span class="sxs-lookup"><span data-stu-id="e5d2e-173">CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</span></span></li>
<li><span data-ttu-id="e5d2e-174">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</span><span class="sxs-lookup"><span data-stu-id="e5d2e-174">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</span></span></li>
<li><span data-ttu-id="e5d2e-175">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e5d2e-175">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="e5d2e-176">0x80880242</span><span class="sxs-lookup"><span data-stu-id="e5d2e-176">0x80880242</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-177"><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-177"><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></span></span></td>
<td><span data-ttu-id="e5d2e-178">La propiedad <a href="attribute-value.md"><strong>Value</strong></a> del objeto de <a href="attribute.md"><strong>atributo</strong></a> no es válida porque el tipo de datos no coincide con el tipo de datos indicado por la propiedad <strong>Name</strong> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-178">The <a href="attribute-value.md"><strong>Value</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object is not valid because the data type does not match the data type indicated by the <strong>Name</strong> property.</span></span> <br/> <span data-ttu-id="e5d2e-179">Por ejemplo, si la propiedad <a href="attribute-value.md"><strong>Name</strong></a> se establece en CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, el tipo de datos debe ser <strong>Date</strong>.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-179">For example, if the <a href="attribute-value.md"><strong>Name</strong></a> property is set to CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, the data type must be <strong>DATE</strong>.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-180">0x80880243</span><span class="sxs-lookup"><span data-stu-id="e5d2e-180">0x80880243</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-181"><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-181"><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-182">No se ha inicializado el objeto de <a href="signer.md"><strong>firmante</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-182">The <a href="signer.md"><strong>Signer</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="e5d2e-183">Para inicializar el objeto de <a href="signer.md"><strong>firmante</strong></a> , establezca la propiedad de <a href="signer-certificate.md"><strong>certificado</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-183">To initialize the <a href="signer.md"><strong>Signer</strong></a> object, set the <a href="signer-certificate.md"><strong>Certificate</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-184">0x80880250</span><span class="sxs-lookup"><span data-stu-id="e5d2e-184">0x80880250</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-185"><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-185"><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></span></span></td>
<td><span data-ttu-id="e5d2e-186">No se encuentra el firmante en el objeto <a href="signeddata.md"><strong>SignedData</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-186">The signer cannot be found in the <a href="signeddata.md"><strong>SignedData</strong></a> object.</span></span> <br/> <span data-ttu-id="e5d2e-187">Normalmente, esto no ocurre con un objeto <a href="signeddata.md"><strong>SignedData</strong></a> creado por CAPICOM; sin embargo, si un producto de terceros creó el objeto <strong>SignedData</strong> , es posible que el certificado del firmante no se incluya en la estructura PKCS #7.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-187">Usually, this does not happen with a <a href="signeddata.md"><strong>SignedData</strong></a> object that was created by CAPICOM; however, if the <strong>SignedData</strong> object was created by a third-party product, the signer's certificate may not be included in the PKCS #7 structure.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-188">0x80880251</span><span class="sxs-lookup"><span data-stu-id="e5d2e-188">0x80880251</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-189"><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-189"><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></span></span></td>
<td><span data-ttu-id="e5d2e-190">No se encuentra un objeto de <a href="chain.md"><strong>cadena</strong></a> en el objeto de <a href="signer.md"><strong>firmante</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-190">A <a href="chain.md"><strong>Chain</strong></a> object cannot be found in the <a href="signer.md"><strong>Signer</strong></a> object.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-191">0x80880252//v 2.0</span><span class="sxs-lookup"><span data-stu-id="e5d2e-191">0x80880252 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-192"><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-192"><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></span></span></td>
<td><span data-ttu-id="e5d2e-193">Se ha intentado usar el firmante de una manera que no es válida.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-193">An attempt is made to use the signer in a way that is not valid.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-194">0x80880253//V2.0</span><span class="sxs-lookup"><span data-stu-id="e5d2e-194">0x80880253 //v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-195"><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-195"><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-196">No se ha inicializado el objeto <a href="signeddata.md"><strong>SignedData</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-196">The <a href="signeddata.md"><strong>SignedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="e5d2e-197">Para inicializar el objeto <a href="signeddata.md"><strong>SignedData</strong></a> , establezca la propiedad <a href="signeddata-content.md"><strong>Content</strong></a> o llame al método <a href="signeddata-verify.md"><strong>Verify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-197">To initialize the <a href="signeddata.md"><strong>SignedData</strong></a> object, set the <a href="signeddata-content.md"><strong>Content</strong></a> property or call the <a href="signeddata-verify.md"><strong>Verify</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-198">0x80880260</span><span class="sxs-lookup"><span data-stu-id="e5d2e-198">0x80880260</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-199"><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-199"><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="e5d2e-200">El objeto <a href="signeddata.md"><strong>SignedData</strong></a> contiene un tipo que no es válido.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-200">The <a href="signeddata.md"><strong>SignedData</strong></a> object contains a type that is not valid.</span></span> <br/> <span data-ttu-id="e5d2e-201">Normalmente, esto sucede cuando se realiza un intento de comprobar un mensaje con doble cifrado con un objeto <a href="signeddata.md"><strong>SignedData</strong></a> o viceversa.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-201">Usually, this happens when an attempt is made to verify an enveloped message with a <a href="signeddata.md"><strong>SignedData</strong></a> object or vice versa.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-202">0x80880261</span><span class="sxs-lookup"><span data-stu-id="e5d2e-202">0x80880261</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-203"><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-203"><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-204">No se firmó el objeto <a href="signeddata.md"><strong>SignedData</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-204">The <a href="signeddata.md"><strong>SignedData</strong></a> object has not been signed.</span></span> <br/> <span data-ttu-id="e5d2e-205">Para firmar el objeto <a href="signeddata.md"><strong>SignedData</strong></a> , llame al método <a href="signeddata-sign.md"><strong>Sign</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-205">To sign the <a href="signeddata.md"><strong>SignedData</strong></a> object, call the <a href="signeddata-sign.md"><strong>Sign</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-206">0x80880262</span><span class="sxs-lookup"><span data-stu-id="e5d2e-206">0x80880262</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-207"><strong>CAPICOM_E_INVALID_ALGORITHM</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-207"><strong>CAPICOM_E_INVALID_ALGORITHM</strong></span></span></td>
<td><span data-ttu-id="e5d2e-208">El valor del algoritmo para la propiedad <a href="algorithm-name.md"><strong>Name</strong></a> del objeto <a href="algorithm.md"><strong>algorithm</strong></a> no es válido.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-208">The algorithm value for the <a href="algorithm-name.md"><strong>Name</strong></a> property of the <a href="algorithm.md"><strong>Algorithm</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="e5d2e-209">En la lista siguiente se muestran los valores de algoritmo válidos para la propiedad <a href="algorithm-name.md"><strong>Name</strong></a> :</span><span class="sxs-lookup"><span data-stu-id="e5d2e-209">The following list shows the valid algorithm values for the <a href="algorithm-name.md"><strong>Name</strong></a> property:</span></span>
<ul>
<li><span data-ttu-id="e5d2e-210">CAPICOM_ENCRYPTION_ALGORITHM_RC2</span><span class="sxs-lookup"><span data-stu-id="e5d2e-210">CAPICOM_ENCRYPTION_ALGORITHM_RC2</span></span></li>
<li><span data-ttu-id="e5d2e-211">CAPICOM_ENCRYPTION_ALGORITHM_RC4</span><span class="sxs-lookup"><span data-stu-id="e5d2e-211">CAPICOM_ENCRYPTION_ALGORITHM_RC4</span></span></li>
<li><span data-ttu-id="e5d2e-212">CAPICOM_ENCRYPTION_ALGORITHM_DES</span><span class="sxs-lookup"><span data-stu-id="e5d2e-212">CAPICOM_ENCRYPTION_ALGORITHM_DES</span></span></li>
<li><span data-ttu-id="e5d2e-213">CAPICOM_ENCRYPTION_ALGORITHM_3DES</span><span class="sxs-lookup"><span data-stu-id="e5d2e-213">CAPICOM_ENCRYPTION_ALGORITHM_3DES</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="e5d2e-214">0x80880270</span><span class="sxs-lookup"><span data-stu-id="e5d2e-214">0x80880270</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-215"><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-215"><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></span></span></td>
<td><span data-ttu-id="e5d2e-216">El valor de longitud de clave para la propiedad <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> del objeto <a href="algorithm.md"><strong>algorithm</strong></a> no es válido.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-216">The key length value for the <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> property of the <a href="algorithm.md"><strong>Algorithm</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="e5d2e-217">En la lista siguiente se muestran los valores de longitud de clave válidos para la propiedad <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> :</span><span class="sxs-lookup"><span data-stu-id="e5d2e-217">The following list shows the valid key length values for the <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> property:</span></span>
<ul>
<li><span data-ttu-id="e5d2e-218">CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</span><span class="sxs-lookup"><span data-stu-id="e5d2e-218">CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</span></span></li>
<li><span data-ttu-id="e5d2e-219">CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</span><span class="sxs-lookup"><span data-stu-id="e5d2e-219">CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</span></span></li>
<li><span data-ttu-id="e5d2e-220">CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</span><span class="sxs-lookup"><span data-stu-id="e5d2e-220">CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</span></span></li>
<li><span data-ttu-id="e5d2e-221">CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</span><span class="sxs-lookup"><span data-stu-id="e5d2e-221">CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="e5d2e-222">0x80880271</span><span class="sxs-lookup"><span data-stu-id="e5d2e-222">0x80880271</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-223"><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-223"><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-224">No se ha inicializado el objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-224">The <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="e5d2e-225">Para inicializar el objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> , establezca la propiedad <a href="envelopeddata-content.md"><strong>Content</strong></a> o llame al método <a href="envelopeddata-decrypt.md"><strong>Decrypt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-225">To initialize the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object, either set the <a href="envelopeddata-content.md"><strong>Content</strong></a> property or call the <a href="envelopeddata-decrypt.md"><strong>Decrypt</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-226">0x80880280</span><span class="sxs-lookup"><span data-stu-id="e5d2e-226">0x80880280</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-227"><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-227"><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="e5d2e-228">El objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> contiene un tipo que no es válido.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-228">The <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object contains a type that is not valid.</span></span> <br/> <span data-ttu-id="e5d2e-229">Normalmente, esto sucede cuando se realiza un intento de comprobar un mensaje firmado con un objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> o viceversa.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-229">Usually, this happens when an attempt is made to verify a signed message with an <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object or vice versa.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-230">0x80880281</span><span class="sxs-lookup"><span data-stu-id="e5d2e-230">0x80880281</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-231"><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-231"><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></span></span></td>
<td><span data-ttu-id="e5d2e-232">No hay ningún destinatario especificado en el objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> cuando se llama al método <a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a> de un objeto <strong>EnvelopedData</strong> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-232">There is no recipient specified in the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object when the <a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a> method of an <strong>EnvelopedData</strong> object is called.</span></span> <br/> <span data-ttu-id="e5d2e-233">Para agregar un destinatario, llame al método <a href="recipients-add.md"><strong>Recipients. Add</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-233">To add a recipient, call the <a href="recipients-add.md"><strong>Recipients.Add</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-234">0x80880282</span><span class="sxs-lookup"><span data-stu-id="e5d2e-234">0x80880282</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-235"><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-235"><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></span></span></td>
<td><span data-ttu-id="e5d2e-236">No se encuentra el destinatario en el objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-236">The recipient cannot be found in the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object.</span></span> <br/> <span data-ttu-id="e5d2e-237">Normalmente, esto no ocurre con un objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> creado por CAPICOM; sin embargo, si un producto de terceros creó el objeto <strong>EnvelopedData</strong> , es posible que el certificado del destinatario no se incluya en la estructura PKCS #7.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-237">Usually, this does not happen with an <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object that was created by CAPICOM; however, if the <strong>EnvelopedData</strong> object was created by a third-party product, the recipient's certificate may not be included in the PKCS #7 structure.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-238">0x80880283</span><span class="sxs-lookup"><span data-stu-id="e5d2e-238">0x80880283</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-239"><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-239"><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-240">El objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-240">The <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="e5d2e-241">Para inicializar el objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> , establezca la propiedad de <a href="encrypteddata-content.md"><strong>contenido</strong></a> o llame al método de <a href="encrypteddata-decrypt.md"><strong>descifrado</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-241">To initialize the <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object, either set the <a href="encrypteddata-content.md"><strong>Content</strong></a> property or call the <a href="encrypteddata-decrypt.md"><strong>Decrypt</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-242">0x80880290</span><span class="sxs-lookup"><span data-stu-id="e5d2e-242">0x80880290</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-243"><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-243"><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="e5d2e-244">El objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> no es un tipo válido.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-244">The <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object is not a valid type.</span></span> <br/> <span data-ttu-id="e5d2e-245">Normalmente, esto significa que los datos están dañados.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-245">Usually, this means the data is corrupted.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-246">0x80880291</span><span class="sxs-lookup"><span data-stu-id="e5d2e-246">0x80880291</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-247"><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-247"><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></span></span></td>
<td><span data-ttu-id="e5d2e-248">El secreto de un objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-248">The secret of an <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="e5d2e-249">Para inicializar el secreto de un objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> , llame al método <a href="encrypteddata-setsecret.md"><strong>SetSecret</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-249">To initialize the secret of an <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object, call the <a href="encrypteddata-setsecret.md"><strong>SetSecret</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-250">0x80880292</span><span class="sxs-lookup"><span data-stu-id="e5d2e-250">0x80880292</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-251"><strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-251"><strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-252">No se ha inicializado el objeto <a href="privatekey.md"><strong>PrivateKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-252">The <a href="privatekey.md"><strong>PrivateKey</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-253">0x80880300//v 2.0</span><span class="sxs-lookup"><span data-stu-id="e5d2e-253">0x80880300 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-254"><strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-254"><strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong></span></span></td>
<td><span data-ttu-id="e5d2e-255">No se puede exportar el objeto <a href="privatekey.md"><strong>PrivateKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-255">The <a href="privatekey.md"><strong>PrivateKey</strong></a> object cannot be exported.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-256">0x80880301//v 2.0</span><span class="sxs-lookup"><span data-stu-id="e5d2e-256">0x80880301 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-257"><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-257"><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-258">No se ha inicializado el objeto <a href="encodeddata.md"><strong>EncodedData</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-258">The <a href="encodeddata.md"><strong>EncodedData</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-259">0x80880320//v 2.0</span><span class="sxs-lookup"><span data-stu-id="e5d2e-259">0x80880320 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-260"><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-260"><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-261">No se ha inicializado el objeto de <a href="extension.md"><strong>extensión</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-261">The <a href="extension.md"><strong>Extension</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-262">0x80880330//v 2.0</span><span class="sxs-lookup"><span data-stu-id="e5d2e-262">0x80880330 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-263"><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-263"><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-264">No se ha inicializado la propiedad <a href="extendedproperty-propid.md"><strong>PropID</strong></a> del objeto <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-264">The <a href="extendedproperty-propid.md"><strong>PropID</strong></a> property of the <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-265">0x80880340//v 2.0</span><span class="sxs-lookup"><span data-stu-id="e5d2e-265">0x80880340 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-266"><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-266"><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="e5d2e-267">El parámetro <em>FindType</em> del método <a href="certificates-find.md"><strong>Certificates. Find</strong></a> no es un valor de la enumeración <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-267">The <em>FindType</em> parameter of the <a href="certificates-find.md"><strong>Certificates.Find</strong></a> method is not a value of the <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> enumeration.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-268">0x80880350//v 2.0</span><span class="sxs-lookup"><span data-stu-id="e5d2e-268">0x80880350 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-269"><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-269"><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></span></span></td>
<td><span data-ttu-id="e5d2e-270">La Directiva predefinida especificada para la operación de búsqueda no es válida.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-270">The specified predefined policy for the find operation is not valid.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-271">0x80880351//v 2.0</span><span class="sxs-lookup"><span data-stu-id="e5d2e-271">0x80880351 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-272"><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-272"><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-273">No se ha inicializado el objeto <a href="signedcode.md"><strong>SignedCode</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-273">The <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-274">0x80880360//v 2.0</span><span class="sxs-lookup"><span data-stu-id="e5d2e-274">0x80880360 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-275"><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-275"><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-276">No se firmó el objeto <a href="signedcode.md"><strong>SignedCode</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-276">The <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been signed.</span></span><br/> <span data-ttu-id="e5d2e-277">Para firmar el objeto <a href="signedcode.md"><strong>SignedCode</strong></a> , llame al método <a href="signedcode-sign.md"><strong>Sign</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-277">To sign the <a href="signedcode.md"><strong>SignedCode</strong></a> object, call the <a href="signedcode-sign.md"><strong>Sign</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-278">0x80880361//v 2.0</span><span class="sxs-lookup"><span data-stu-id="e5d2e-278">0x80880361 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-279"><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-279"><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-280">No se ha inicializado la propiedad <a href="signedcode-description.md"><strong>Description</strong></a> del objeto <a href="signedcode.md"><strong>SignedCode</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-280">The <a href="signedcode-description.md"><strong>Description</strong></a> property of the <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-281">0x80880362//v 2.0</span><span class="sxs-lookup"><span data-stu-id="e5d2e-281">0x80880362 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-282"><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-282"><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-283">No se ha inicializado la propiedad <a href="signedcode-descriptionurl.md"><strong>DescriptionURL</strong></a> del objeto <a href="signedcode.md"><strong>SignedCode</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-283">The <a href="signedcode-descriptionurl.md"><strong>DescriptionURL</strong></a> property of the <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-284">0x80880363//v 2.0</span><span class="sxs-lookup"><span data-stu-id="e5d2e-284">0x80880363 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-285"><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-285"><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></span></span></td>
<td><span data-ttu-id="e5d2e-286">El parámetro de <em>dirección URL</em> del método <a href="signedcode-timestamp.md"><strong>SignedCode. timestamp</strong></a> no es válido.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-286">The <em>URL</em> parameter of the <a href="signedcode-timestamp.md"><strong>SignedCode.Timestamp</strong></a> method is not valid.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-287">0x80880364//v 2.0</span><span class="sxs-lookup"><span data-stu-id="e5d2e-287">0x80880364 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-288"><strong>CAPICOM_E_HASH_NO_DATA</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-288"><strong>CAPICOM_E_HASH_NO_DATA</strong></span></span></td>
<td><span data-ttu-id="e5d2e-289">El objeto <a href="hasheddata.md"><strong>HashedData</strong></a> no contiene ningún dato.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-289">The <a href="hasheddata.md"><strong>HashedData</strong></a> object does not contain any data.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-290">0x80880370//v 2.0</span><span class="sxs-lookup"><span data-stu-id="e5d2e-290">0x80880370 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-291"><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-291"><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></span></span></td>
<td><span data-ttu-id="e5d2e-292">El tipo de conversión no es válido.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-292">The convert type is not valid.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-293">0x80880380//v 2.0</span><span class="sxs-lookup"><span data-stu-id="e5d2e-293">0x80880380 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-294"><strong>CAPICOM_E_NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-294"><strong>CAPICOM_E_NOT_SUPPORTED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-295">La operación solicitada no se admite en la plataforma actual.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-295">The requested operation is not supported in the current platform.</span></span> <br/></td>
<td><span data-ttu-id="e5d2e-296">0x80880900</span><span class="sxs-lookup"><span data-stu-id="e5d2e-296">0x80880900</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-297"><strong>CAPICOM_E_UI_DISABLED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-297"><strong>CAPICOM_E_UI_DISABLED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-298">Al firmar, no se ha establecido la propiedad de <a href="signer-certificate.md"><strong>certificado</strong></a> del objeto de <a href="signer.md"><strong>firmante</strong></a> , pero se ha deshabilitado el símbolo del sistema para el certificado de usuario.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-298">When signing, the <a href="signer-certificate.md"><strong>Certificate</strong></a> property of the <a href="signer.md"><strong>Signer</strong></a> object has not been set, but the prompt for the user certificate has been disabled.</span></span> <br/> <span data-ttu-id="e5d2e-299">Habilite el símbolo del sistema estableciendo la propiedad <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> del objeto de <a href="settings.md"><strong>configuración</strong></a> o establezca la propiedad de <a href="signer-certificate.md"><strong>certificado</strong></a> del objeto de <a href="signer.md"><strong>firmante</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5d2e-299">Either enable the prompt by setting the <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> property of the <a href="settings.md"><strong>Settings</strong></a> object, or set the <a href="signer-certificate.md"><strong>Certificate</strong></a> property of the <a href="signer.md"><strong>Signer</strong></a> object.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-300">0x80880901</span><span class="sxs-lookup"><span data-stu-id="e5d2e-300">0x80880901</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-301"><strong>CAPICOM_E_CANCELLED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-301"><strong>CAPICOM_E_CANCELLED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-302">El usuario ha cancelado la operación.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-302">The operation has been canceled by the user.</span></span> <br/> <span data-ttu-id="e5d2e-303">Esto sucede cuando se solicita al usuario permiso para llevar a cabo una operación determinada, como tener acceso a la clave privada, y el usuario cancela la operación.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-303">This happens when the user is prompted for permission to carry out a certain operation, such as accessing the private key, and the user cancels the operation.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-304">0x80880902</span><span class="sxs-lookup"><span data-stu-id="e5d2e-304">0x80880902</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-305"><strong>CAPICOM_E_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-305"><strong>CAPICOM_E_NOT_ALLOWED</strong></span></span></td>
<td><span data-ttu-id="e5d2e-306">La operación intentada no está permitida.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-306">The attempted operation is not allowed.</span></span><br/> <span data-ttu-id="e5d2e-307">Por ejemplo, no se permite cambiar la propiedad <a href="extendedproperty-propid.md"><strong>PropID</strong></a> de un objeto <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> si el objeto está asociado a un certificado.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-307">For example, changing the <a href="extendedproperty-propid.md"><strong>PropID</strong></a> property of an <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> object is not allowed if the object is attached to a certificate.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-308">0x80880903//v 2.0</span><span class="sxs-lookup"><span data-stu-id="e5d2e-308">0x80880903 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-309"><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-309"><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></span></span></td>
<td><span data-ttu-id="e5d2e-310">CAPICOM se ha quedado sin recursos.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-310">CAPICOM has run out of a resource.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-311">0x80880904//v 2.0</span><span class="sxs-lookup"><span data-stu-id="e5d2e-311">0x80880904 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2e-312"><strong>CAPICOM_E_INTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-312"><strong>CAPICOM_E_INTERNAL</strong></span></span></td>
<td><span data-ttu-id="e5d2e-313">Se ha producido un error interno.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-313">An internal error has occurred.</span></span> <br/> <span data-ttu-id="e5d2e-314">Póngase en contacto con el soporte técnico de Microsoft para obtener ayuda.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-314">Contact Microsoft Technical Support for assistance.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-315">0x80880911</span><span class="sxs-lookup"><span data-stu-id="e5d2e-315">0x80880911</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2e-316"><strong>CAPICOM_E_UNKNOWN</strong></span><span class="sxs-lookup"><span data-stu-id="e5d2e-316"><strong>CAPICOM_E_UNKNOWN</strong></span></span></td>
<td><span data-ttu-id="e5d2e-317">Se ha producido un error desconocido.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-317">An unknown error has occurred.</span></span> <br/> <span data-ttu-id="e5d2e-318">Recopile tanta información como sea posible y póngase en contacto con su proveedor.</span><span class="sxs-lookup"><span data-stu-id="e5d2e-318">Collect as much information as possible, and contact your vendor.</span></span><br/></td>
<td><span data-ttu-id="e5d2e-319">0x80880999</span><span class="sxs-lookup"><span data-stu-id="e5d2e-319">0x80880999</span></span></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="e5d2e-320">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5d2e-320">Requirements</span></span>



| <span data-ttu-id="e5d2e-321">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5d2e-321">Requirement</span></span> | <span data-ttu-id="e5d2e-322">Value</span><span class="sxs-lookup"><span data-stu-id="e5d2e-322">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e5d2e-323">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="e5d2e-323">Redistributable</span></span><br/> | <span data-ttu-id="e5d2e-324">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="e5d2e-324">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="e5d2e-325">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5d2e-325">Header</span></span><br/>          | <dl> <span data-ttu-id="e5d2e-326"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5d2e-326"><dt>Capicom.h</dt></span></span> </dl> |



 

 




