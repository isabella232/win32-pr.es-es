---
description: Representa la clave privada asociada a un certificado.
ms.assetid: 26ad1d1c-17c5-4191-ac97-b911e62b4119
title: Objeto PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e87ca7a5bf12bbaf943bccacaa075a51ae75ed37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670437"
---
# <a name="privatekey-object"></a><span data-ttu-id="854a4-103">Objeto PrivateKey</span><span class="sxs-lookup"><span data-stu-id="854a4-103">PrivateKey object</span></span>

<span data-ttu-id="854a4-104">\[El objeto **PrivateKey** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="854a4-104">\[The **PrivateKey** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="854a4-105">En su lugar, use la [**propiedad X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="854a4-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="854a4-106">El objeto **PrivateKey** representa la [*clave privada*](../secgloss/p-gly.md) asociada a un certificado.</span><span class="sxs-lookup"><span data-stu-id="854a4-106">The **PrivateKey** object represents the [*private key*](../secgloss/p-gly.md) associated with a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="854a4-107">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="854a4-107">When to use</span></span>

<span data-ttu-id="854a4-108">El objeto **PrivateKey** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="854a4-108">The **PrivateKey** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="854a4-109">Recuperar información acerca de la clave privada.</span><span class="sxs-lookup"><span data-stu-id="854a4-109">Retrieve information about the private key.</span></span>
-   <span data-ttu-id="854a4-110">Abra el contenedor de claves privadas.</span><span class="sxs-lookup"><span data-stu-id="854a4-110">Open the private key container.</span></span>
-   <span data-ttu-id="854a4-111">Elimine la clave privada.</span><span class="sxs-lookup"><span data-stu-id="854a4-111">Delete the private key.</span></span>

## <a name="members"></a><span data-ttu-id="854a4-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="854a4-112">Members</span></span>

<span data-ttu-id="854a4-113">El objeto **PrivateKey** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="854a4-113">The **PrivateKey** object has these types of members:</span></span>

-   [<span data-ttu-id="854a4-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="854a4-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="854a4-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="854a4-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="854a4-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="854a4-116">Methods</span></span>

<span data-ttu-id="854a4-117">El objeto **PrivateKey** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="854a4-117">The **PrivateKey** object has these methods.</span></span>



| <span data-ttu-id="854a4-118">Método</span><span class="sxs-lookup"><span data-stu-id="854a4-118">Method</span></span>                                                  | <span data-ttu-id="854a4-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="854a4-119">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="854a4-120">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="854a4-120">**Delete**</span></span>](privatekey-delete.md)                     | <span data-ttu-id="854a4-121">Elimina el contenedor de claves privadas al que hace referencia el objeto **PrivateKey** .</span><span class="sxs-lookup"><span data-stu-id="854a4-121">Deletes the private key container referenced by the **PrivateKey** object.</span></span><br/>                                                                                |
| [<span data-ttu-id="854a4-122">**IsAccessible**</span><span class="sxs-lookup"><span data-stu-id="854a4-122">**IsAccessible**</span></span>](privatekey-isaccessible.md)         | <span data-ttu-id="854a4-123">Recupera un valor booleano que indica si el usuario puede tener acceso a la clave privada.</span><span class="sxs-lookup"><span data-stu-id="854a4-123">Retrieves a Boolean value that indicates whether the private key is accessible by the user.</span></span> <span data-ttu-id="854a4-124">Si es true, el usuario puede tener acceso a la clave privada.</span><span class="sxs-lookup"><span data-stu-id="854a4-124">If true, the user can access the private key.</span></span><br/>                 |
| [<span data-ttu-id="854a4-125">**IsExportable**</span><span class="sxs-lookup"><span data-stu-id="854a4-125">**IsExportable**</span></span>](privatekey-isexportable.md)         | <span data-ttu-id="854a4-126">Recupera un valor booleano que indica si se puede exportar la clave privada.</span><span class="sxs-lookup"><span data-stu-id="854a4-126">Retrieves a Boolean value that indicates whether the private key can be exported.</span></span> <span data-ttu-id="854a4-127">Si es true, se puede exportar la clave privada.</span><span class="sxs-lookup"><span data-stu-id="854a4-127">If true, the private key can be exported.</span></span><br/>                               |
| [<span data-ttu-id="854a4-128">**IsHardwareDevice**</span><span class="sxs-lookup"><span data-stu-id="854a4-128">**IsHardwareDevice**</span></span>](privatekey-ishardwaredevice.md) | <span data-ttu-id="854a4-129">Recupera un valor booleano que indica si la clave privada está almacenada en un dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="854a4-129">Retrieves a Boolean value that indicates whether the private key is stored on a hardware device.</span></span> <span data-ttu-id="854a4-130">Si es true, la clave privada se almacena en un dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="854a4-130">If true, the private key is stored on a hardware device.</span></span><br/> |
| [<span data-ttu-id="854a4-131">**IsMachineKeyset**</span><span class="sxs-lookup"><span data-stu-id="854a4-131">**IsMachineKeyset**</span></span>](privatekey-ismachinekeyset.md)   | <span data-ttu-id="854a4-132">Recupera un valor booleano que indica si la clave privada es una clave de equipo.</span><span class="sxs-lookup"><span data-stu-id="854a4-132">Retrieves a Boolean value that indicates whether the private key is a machine key.</span></span> <span data-ttu-id="854a4-133">Si es true, la clave privada es una clave de equipo.</span><span class="sxs-lookup"><span data-stu-id="854a4-133">If true, the private key is a machine key.</span></span><br/>                             |
| [<span data-ttu-id="854a4-134">**IsProtected**</span><span class="sxs-lookup"><span data-stu-id="854a4-134">**IsProtected**</span></span>](privatekey-isprotected.md)           | <span data-ttu-id="854a4-135">Recupera un valor booleano que indica si la clave privada está protegida.</span><span class="sxs-lookup"><span data-stu-id="854a4-135">Retrieves a Boolean value that indicates whether the private key is protected.</span></span> <span data-ttu-id="854a4-136">Si es true, la clave privada está protegida.</span><span class="sxs-lookup"><span data-stu-id="854a4-136">If true, the private key is protected.</span></span><br/>                                     |
| [<span data-ttu-id="854a4-137">**IsRemovable**</span><span class="sxs-lookup"><span data-stu-id="854a4-137">**IsRemovable**</span></span>](privatekey-isremovable.md)           | <span data-ttu-id="854a4-138">Recupera un valor booleano que indica si la clave privada está en un dispositivo extraíble.</span><span class="sxs-lookup"><span data-stu-id="854a4-138">Retrieves a Boolean value that indicates whether the private key is on a removable device.</span></span> <span data-ttu-id="854a4-139">Si es true, la clave privada se encuentra en un dispositivo extraíble.</span><span class="sxs-lookup"><span data-stu-id="854a4-139">If true, the private key is on a removable device.</span></span><br/>             |
| [<span data-ttu-id="854a4-140">**Ábra**</span><span class="sxs-lookup"><span data-stu-id="854a4-140">**Open**</span></span>](privatekey-open.md)                         | <span data-ttu-id="854a4-141">Obtiene acceso a un contenedor de claves existente.</span><span class="sxs-lookup"><span data-stu-id="854a4-141">Accesses an existing key container.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="854a4-142">Propiedades</span><span class="sxs-lookup"><span data-stu-id="854a4-142">Properties</span></span>

<span data-ttu-id="854a4-143">El objeto **PrivateKey** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="854a4-143">The **PrivateKey** object has these properties.</span></span>



| <span data-ttu-id="854a4-144">Propiedad</span><span class="sxs-lookup"><span data-stu-id="854a4-144">Property</span></span>                                                                 | <span data-ttu-id="854a4-145">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="854a4-145">Access type</span></span>          | <span data-ttu-id="854a4-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="854a4-146">Description</span></span>                                                                                               |
|:-------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="854a4-147">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="854a4-147">**ContainerName**</span></span>](privatekey-containername.md)<br/>             | <span data-ttu-id="854a4-148">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="854a4-148">Read-only</span></span><br/> | <span data-ttu-id="854a4-149">Recupera una cadena que contiene el nombre del contenedor de claves privadas.</span><span class="sxs-lookup"><span data-stu-id="854a4-149">Retrieves a string that contains the private key container name.</span></span> <span data-ttu-id="854a4-150">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="854a4-150">This is the default property.</span></span><br/> |
| [<span data-ttu-id="854a4-151">**Especificación**</span><span class="sxs-lookup"><span data-stu-id="854a4-151">**KeySpec**</span></span>](privatekey-keyspec.md)<br/>                         | <span data-ttu-id="854a4-152">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="854a4-152">Read-only</span></span><br/> | <span data-ttu-id="854a4-153">Recupera la especificación de clave.</span><span class="sxs-lookup"><span data-stu-id="854a4-153">Retrieves the key specification.</span></span><br/>                                                               |
| [<span data-ttu-id="854a4-154">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="854a4-154">**ProviderName**</span></span>](privatekey-providername.md)<br/>               | <span data-ttu-id="854a4-155">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="854a4-155">Read-only</span></span><br/> | <span data-ttu-id="854a4-156">Recupera una cadena que contiene el nombre del CSP.</span><span class="sxs-lookup"><span data-stu-id="854a4-156">Retrieves a string that contains the name of the CSP.</span></span><br/>                                          |
| [<span data-ttu-id="854a4-157">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="854a4-157">**ProviderType**</span></span>](privatekey-providertype.md)<br/>               | <span data-ttu-id="854a4-158">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="854a4-158">Read-only</span></span><br/> | <span data-ttu-id="854a4-159">Recupera un valor de enumeración que especifica el tipo de proveedor.</span><span class="sxs-lookup"><span data-stu-id="854a4-159">Retrieves an enumeration value that specifies the type of provider.</span></span><br/>                            |
| [<span data-ttu-id="854a4-160">**UniqueContainerName**</span><span class="sxs-lookup"><span data-stu-id="854a4-160">**UniqueContainerName**</span></span>](privatekey-uniquecontainername.md)<br/> | <span data-ttu-id="854a4-161">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="854a4-161">Read-only</span></span><br/> | <span data-ttu-id="854a4-162">Recupera una cadena que contiene el nombre único del contenedor de claves privadas.</span><span class="sxs-lookup"><span data-stu-id="854a4-162">Retrieves a string that contains the unique private key container name.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="854a4-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="854a4-163">Remarks</span></span>

<span data-ttu-id="854a4-164">Se puede crear el objeto **PrivateKey** y es seguro para el scripting.</span><span class="sxs-lookup"><span data-stu-id="854a4-164">The **PrivateKey** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="854a4-165">El ProgID del objeto **PrivateKey** es CAPICOM. PrivateKey. 1.</span><span class="sxs-lookup"><span data-stu-id="854a4-165">The ProgID for the **PrivateKey** object is CAPICOM.PrivateKey.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="854a4-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="854a4-166">Requirements</span></span>



| <span data-ttu-id="854a4-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="854a4-167">Requirement</span></span> | <span data-ttu-id="854a4-168">Value</span><span class="sxs-lookup"><span data-stu-id="854a4-168">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="854a4-169">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="854a4-169">Redistributable</span></span><br/> | <span data-ttu-id="854a4-170">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="854a4-170">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="854a4-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="854a4-171">DLL</span></span><br/>             | <dl> <span data-ttu-id="854a4-172"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="854a4-172"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
