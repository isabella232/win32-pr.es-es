---
description: Proporciona funcionalidad para firmar archivos ejecutables con una firma digital Authenticode.
ms.assetid: e6d4e694-471f-4d30-983c-6bc5d631d99e
title: Objeto SignedCode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 08648c8b941874a6d1e1ed97d49f510694b998b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671644"
---
# <a name="signedcode-object"></a><span data-ttu-id="383d6-103">Objeto SignedCode</span><span class="sxs-lookup"><span data-stu-id="383d6-103">SignedCode object</span></span>

<span data-ttu-id="383d6-104">\[El objeto **SignedCode** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="383d6-104">\[The **SignedCode** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="383d6-105">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API Win32 para firmar el contenido con una firma digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="383d6-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="383d6-106">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="383d6-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="383d6-107">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="383d6-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="383d6-108">El objeto **SignedCode** proporciona funcionalidad para firmar archivos ejecutables con una firma digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="383d6-108">The **SignedCode** object provides functionality for signing executable files with an Authenticode digital signature.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="383d6-109">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="383d6-109">When to use</span></span>

<span data-ttu-id="383d6-110">El objeto **SignedCode** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="383d6-110">The **SignedCode** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="383d6-111">Firmar archivos ejecutables.</span><span class="sxs-lookup"><span data-stu-id="383d6-111">Sign executable files.</span></span>
-   <span data-ttu-id="383d6-112">Archivos ejecutables de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="383d6-112">Time stamp executable files.</span></span>
-   <span data-ttu-id="383d6-113">Determine si la firma del archivo ejecutable es válida.</span><span class="sxs-lookup"><span data-stu-id="383d6-113">Determine whether the signature of the executable file is valid.</span></span>
-   <span data-ttu-id="383d6-114">Establezca o recupere la ruta de acceso al archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="383d6-114">Set or retrieve the path to the executable file.</span></span>
-   <span data-ttu-id="383d6-115">Recupere el autor de firma y hora del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="383d6-115">Retrieve the signer and time stamper of the executable file.</span></span>
-   <span data-ttu-id="383d6-116">Recupera una colección de los certificados para el archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="383d6-116">Retrieve a collection of the certificates for the executable file.</span></span>
-   <span data-ttu-id="383d6-117">Recupere una descripción o la dirección URL de la descripción del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="383d6-117">Retrieve a description or the URL to the description of the executable file.</span></span>

## <a name="members"></a><span data-ttu-id="383d6-118">Miembros</span><span class="sxs-lookup"><span data-stu-id="383d6-118">Members</span></span>

<span data-ttu-id="383d6-119">El objeto **SignedCode** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="383d6-119">The **SignedCode** object has these types of members:</span></span>

-   [<span data-ttu-id="383d6-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="383d6-120">Methods</span></span>](#methods)
-   [<span data-ttu-id="383d6-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="383d6-121">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="383d6-122">Métodos</span><span class="sxs-lookup"><span data-stu-id="383d6-122">Methods</span></span>

<span data-ttu-id="383d6-123">El objeto **SignedCode** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="383d6-123">The **SignedCode** object has these methods.</span></span>



| <span data-ttu-id="383d6-124">Método</span><span class="sxs-lookup"><span data-stu-id="383d6-124">Method</span></span>                                    | <span data-ttu-id="383d6-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="383d6-125">Description</span></span>                                                                                                                                                         |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="383d6-126">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="383d6-126">**Sign**</span></span>](signedcode-sign.md)           | <span data-ttu-id="383d6-127">Crea una firma digital Authenticode y firma el archivo ejecutable especificado en la propiedad [**SignedCode. FileName**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="383d6-127">Creates an Authenticode digital signature and signs the executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/>    |
| [<span data-ttu-id="383d6-128">**Indicaciones**</span><span class="sxs-lookup"><span data-stu-id="383d6-128">**Timestamp**</span></span>](signedcode-timestamp.md) | <span data-ttu-id="383d6-129">Crea una firma de marca de tiempo Authenticode en el archivo ejecutable firmado especificado en la propiedad [**SignedCode. FileName**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="383d6-129">Creates an Authenticode time stamp signature on the signed executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/> |
| [<span data-ttu-id="383d6-130">**Ver**</span><span class="sxs-lookup"><span data-stu-id="383d6-130">**Verify**</span></span>](signedcode-verify.md)       | <span data-ttu-id="383d6-131">Comprueba la firma Authenticode del archivo ejecutable firmado especificado en la propiedad [**SignedCode. FileName**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="383d6-131">Verifies the Authenticode signature on the signed executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="383d6-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="383d6-132">Properties</span></span>

<span data-ttu-id="383d6-133">El objeto **SignedCode** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="383d6-133">The **SignedCode** object has these properties.</span></span>



| <span data-ttu-id="383d6-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="383d6-134">Property</span></span>                                                       | <span data-ttu-id="383d6-135">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="383d6-135">Access type</span></span>           | <span data-ttu-id="383d6-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="383d6-136">Description</span></span>                                                                                                                                |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="383d6-137">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="383d6-137">**Certificates**</span></span>](signedcode-certificates.md)<br/>     | <span data-ttu-id="383d6-138">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="383d6-138">Read-only</span></span><br/>  | <span data-ttu-id="383d6-139">Colección de [**certificados**](certificates.md) que contiene todos los certificados del archivo ejecutable firmado.</span><span class="sxs-lookup"><span data-stu-id="383d6-139">A [**Certificates**](certificates.md) collection that contains all the certificates in the signed executable file.</span></span><br/>             |
| [<span data-ttu-id="383d6-140">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="383d6-140">**Description**</span></span>](signedcode-description.md)<br/>       | <span data-ttu-id="383d6-141">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="383d6-141">Read/write</span></span><br/> | <span data-ttu-id="383d6-142">Una cadena que contiene una descripción del archivo ejecutable firmado.</span><span class="sxs-lookup"><span data-stu-id="383d6-142">A string that contains a description of the signed executable file.</span></span><br/>                                                             |
| [<span data-ttu-id="383d6-143">**DescriptionURL**</span><span class="sxs-lookup"><span data-stu-id="383d6-143">**DescriptionURL**</span></span>](signedcode-descriptionurl.md)<br/> | <span data-ttu-id="383d6-144">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="383d6-144">Read/write</span></span><br/> | <span data-ttu-id="383d6-145">Una cadena que contiene la dirección HTTP a una descripción del archivo ejecutable firmado.</span><span class="sxs-lookup"><span data-stu-id="383d6-145">A string that contains the HTTP address to a description of the signed executable file.</span></span><br/>                                         |
| [<span data-ttu-id="383d6-146">**Extensión**</span><span class="sxs-lookup"><span data-stu-id="383d6-146">**FileName**</span></span>](signedcode-filename.md)<br/>             | <span data-ttu-id="383d6-147">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="383d6-147">Read/write</span></span><br/> | <span data-ttu-id="383d6-148">Cadena que contiene la ruta de acceso al archivo de contenido que contiene el archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="383d6-148">A string that contains the path to the content file that contains the executable file.</span></span><br/> <span data-ttu-id="383d6-149">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="383d6-149">This is the default property.</span></span><br/> |
| [<span data-ttu-id="383d6-150">**Firmante**</span><span class="sxs-lookup"><span data-stu-id="383d6-150">**Signer**</span></span>](signedcode-signer.md)<br/>                 | <span data-ttu-id="383d6-151">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="383d6-151">Read-only</span></span><br/>  | <span data-ttu-id="383d6-152">Objeto de [**firmante**](signer.md) que proporciona acceso al firmante del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="383d6-152">A [**Signer**](signer.md) object that provides access to the signer of the executable file.</span></span><br/>                                    |
| [<span data-ttu-id="383d6-153">**Marca de tiempo**</span><span class="sxs-lookup"><span data-stu-id="383d6-153">**Timestamper**</span></span>](signedcode-timestamper.md)<br/>       | <span data-ttu-id="383d6-154">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="383d6-154">Read-only</span></span><br/>  | <span data-ttu-id="383d6-155">Objeto de [**firmante**](signer.md) que proporciona acceso a la autor horaria del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="383d6-155">A [**Signer**](signer.md) object that provides access to the time stamper of the executable file.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="383d6-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="383d6-156">Remarks</span></span>

<span data-ttu-id="383d6-157">El objeto **SignedCode** se puede crear y no es seguro para el scripting.</span><span class="sxs-lookup"><span data-stu-id="383d6-157">The **SignedCode** object can be created, and is not safe for scripting.</span></span> <span data-ttu-id="383d6-158">El ProgID del objeto **SignedCode** es CAPICOM. SignedCode. 1.</span><span class="sxs-lookup"><span data-stu-id="383d6-158">The ProgID for the **SignedCode** object is CAPICOM.SignedCode.1.</span></span>

<span data-ttu-id="383d6-159">El archivo ejecutable debe ser de un tipo que se pueda firmar con la tecnología Authenticode; por ejemplo, los archivos que tienen una extensión de nombre de archivo. cab,. cat,. exe,. dll,. vbs o. ocx.</span><span class="sxs-lookup"><span data-stu-id="383d6-159">The executable file should be of a type that can be signed with Authenticode technology, for example, files that have a file name extension of .cab, .cat, .exe, .dll, .vbs, or .ocx.</span></span>

## <a name="requirements"></a><span data-ttu-id="383d6-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="383d6-160">Requirements</span></span>



| <span data-ttu-id="383d6-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="383d6-161">Requirement</span></span> | <span data-ttu-id="383d6-162">Value</span><span class="sxs-lookup"><span data-stu-id="383d6-162">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="383d6-163">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="383d6-163">Redistributable</span></span><br/> | <span data-ttu-id="383d6-164">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="383d6-164">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="383d6-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="383d6-165">DLL</span></span><br/>             | <dl> <span data-ttu-id="383d6-166"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="383d6-166"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
