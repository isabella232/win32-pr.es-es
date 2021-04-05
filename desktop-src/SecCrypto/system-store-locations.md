---
description: Un almacén del sistema es una colección que consta de uno o varios almacenes físicos del mismo nivel.
ms.assetid: 41fe9366-4c17-43bb-91d6-934c7aa87a2d
title: Ubicaciones del almacén del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0863ffde8be5db67459908b1ec26ec73da029744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002081"
---
# <a name="system-store-locations"></a><span data-ttu-id="8f184-103">Ubicaciones del almacén del sistema</span><span class="sxs-lookup"><span data-stu-id="8f184-103">System Store Locations</span></span>

<span data-ttu-id="8f184-104">Un almacén del sistema es una colección que consta de uno o varios almacenes físicos del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="8f184-104">A system store is a collection that consists of one or more physical sibling stores.</span></span> <span data-ttu-id="8f184-105">En cada almacén del sistema hay almacenes físicos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="8f184-105">For each system store, there are predefined physical sibling stores.</span></span> <span data-ttu-id="8f184-106">Después de abrir un almacén del sistema como mi en CERT \_ System \_ Store \_ Current \_ User, el proveedor de almacén llama a [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) para abrir cada uno de los almacenes físicos en la colección de almacenes del sistema.</span><span class="sxs-lookup"><span data-stu-id="8f184-106">After opening a system store such as MY at CERT\_SYSTEM\_STORE\_CURRENT\_USER, the store provider calls [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) to open each of the physical stores in the system store collection.</span></span> <span data-ttu-id="8f184-107">En el proceso de apertura, cada uno de estos almacenes físicos se agrega a la colección de almacenes del sistema mediante [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection).</span><span class="sxs-lookup"><span data-stu-id="8f184-107">In the open process, each of these physical stores is added to the system store collection using [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection).</span></span> <span data-ttu-id="8f184-108">Todos los certificados de esos almacenes físicos están disponibles a través de la colección de almacenes lógicos del sistema.</span><span class="sxs-lookup"><span data-stu-id="8f184-108">All certificates in those physical stores are available through the logical system store collection.</span></span>

<span data-ttu-id="8f184-109">Para cada ubicación del almacén del sistema, los almacenes de sistemas predefinidos son:</span><span class="sxs-lookup"><span data-stu-id="8f184-109">For each system store location, the predefined systems stores are:</span></span>

-   <span data-ttu-id="8f184-110">MY</span><span class="sxs-lookup"><span data-stu-id="8f184-110">MY</span></span>
-   <span data-ttu-id="8f184-111">Root</span><span class="sxs-lookup"><span data-stu-id="8f184-111">Root</span></span>
-   <span data-ttu-id="8f184-112">Confianza</span><span class="sxs-lookup"><span data-stu-id="8f184-112">Trust</span></span>
-   <span data-ttu-id="8f184-113">CA</span><span class="sxs-lookup"><span data-stu-id="8f184-113">CA</span></span>

<span data-ttu-id="8f184-114">En CERT \_ System \_ Store \_ \_ el usuario actual, también hay un almacén UserDS predefinido.</span><span class="sxs-lookup"><span data-stu-id="8f184-114">In CERT\_SYSTEM\_STORE\_CURRENT\_USER, there is also a predefined UserDS store.</span></span> <span data-ttu-id="8f184-115">Se planea una tienda de tarjetas inteligentes para esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="8f184-115">A smart card store is planned for this location.</span></span>

<span data-ttu-id="8f184-116">Estos son los almacenes del sistema seguidos de comentarios adicionales:</span><span class="sxs-lookup"><span data-stu-id="8f184-116">Here are the system stores followed by further remarks:</span></span>

-   [<span data-ttu-id="8f184-117">\_ \_ usuario actual del almacén del sistema \_ CERT \_</span><span class="sxs-lookup"><span data-stu-id="8f184-117">CERT\_SYSTEM\_STORE\_CURRENT\_USER</span></span>](#cert_system_store_current_user)
-   [<span data-ttu-id="8f184-118">\_ \_ máquina local del almacén del sistema \_ CERT \_</span><span class="sxs-lookup"><span data-stu-id="8f184-118">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>](#cert_system_store_local_machine)
-   [<span data-ttu-id="8f184-119">\_ \_ servicio actual del almacén del sistema \_ de certificados \_</span><span class="sxs-lookup"><span data-stu-id="8f184-119">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE</span></span>](#cert_system_store_current_service)
-   [<span data-ttu-id="8f184-120">\_servicios del \_ almacén del sistema de certificados \_</span><span class="sxs-lookup"><span data-stu-id="8f184-120">CERT\_SYSTEM\_STORE\_SERVICES</span></span>](#cert_system_store_services)
-   [<span data-ttu-id="8f184-121">\_usuarios del \_ almacén del sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="8f184-121">CERT\_SYSTEM\_STORE\_USERS</span></span>](#cert_system_store_users)
-   [<span data-ttu-id="8f184-122">\_Directiva de \_ \_ grupo de usuario actual del \_ sistema \_ de certificados</span><span class="sxs-lookup"><span data-stu-id="8f184-122">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY</span></span>](#cert_system_current_user_group_policy)
-   [<span data-ttu-id="8f184-123">\_Directiva de \_ \_ Grupo del equipo local \_ \_ del sistema de certificados</span><span class="sxs-lookup"><span data-stu-id="8f184-123">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>](#cert_system_local_machine_group_policy)
-   [<span data-ttu-id="8f184-124">certificado de la \_ \_ \_ máquina local del almacén \_ del sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="8f184-124">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE</span></span>](#cert_system_store_local_machine_enterprise)
-   [<span data-ttu-id="8f184-125">Comentarios:</span><span class="sxs-lookup"><span data-stu-id="8f184-125">Remarks</span></span>](#remarks)

### <a name="cert_system_store_current_user"></a><span data-ttu-id="8f184-126">\_ \_ usuario actual del almacén del sistema \_ CERT \_</span><span class="sxs-lookup"><span data-stu-id="8f184-126">CERT\_SYSTEM\_STORE\_CURRENT\_USER</span></span>

<span data-ttu-id="8f184-127">\_ \_ \_ Los almacenes del sistema del usuario actual del almacén del sistema \_ de certificados se encuentran en la siguiente ubicación del registro:</span><span class="sxs-lookup"><span data-stu-id="8f184-127">CERT\_SYSTEM\_STORE\_CURRENT\_USER system stores are at the following registry location:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         SystemCertificates
```

<span data-ttu-id="8f184-128">Los almacenes físicos predefinidos asociados a esos almacenes del sistema son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="8f184-128">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="8f184-129">Almacén del sistema</span><span class="sxs-lookup"><span data-stu-id="8f184-129">System store</span></span> | <span data-ttu-id="8f184-130">Almacén físico</span><span class="sxs-lookup"><span data-stu-id="8f184-130">Physical store</span></span>                                           |
|--------------|----------------------------------------------------------|
| <span data-ttu-id="8f184-131">MY</span><span class="sxs-lookup"><span data-stu-id="8f184-131">MY</span></span>           | <span data-ttu-id="8f184-132">. Predeterminada</span><span class="sxs-lookup"><span data-stu-id="8f184-132">.Default</span></span>                                                 |
| <span data-ttu-id="8f184-133">Root</span><span class="sxs-lookup"><span data-stu-id="8f184-133">Root</span></span>         | <span data-ttu-id="8f184-134">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="8f184-134">.Default.LocalMachine</span></span><br/> <span data-ttu-id="8f184-135">. Tarjeta</span><span class="sxs-lookup"><span data-stu-id="8f184-135">.SmartCard</span></span><br/>   |
| <span data-ttu-id="8f184-136">Confianza</span><span class="sxs-lookup"><span data-stu-id="8f184-136">Trust</span></span>        | <span data-ttu-id="8f184-137">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="8f184-137">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="8f184-138">. Almacén</span><span class="sxs-lookup"><span data-stu-id="8f184-138">.LocalMachine</span></span><br/> |
| <span data-ttu-id="8f184-139">CA</span><span class="sxs-lookup"><span data-stu-id="8f184-139">CA</span></span>           | <span data-ttu-id="8f184-140">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="8f184-140">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="8f184-141">. Almacén</span><span class="sxs-lookup"><span data-stu-id="8f184-141">.LocalMachine</span></span><br/> |
| <span data-ttu-id="8f184-142">UserDS</span><span class="sxs-lookup"><span data-stu-id="8f184-142">UserDS</span></span>       | <span data-ttu-id="8f184-143">. UserCertificate</span><span class="sxs-lookup"><span data-stu-id="8f184-143">.UserCertificate</span></span>                                         |



 

### <a name="cert_system_store_local_machine"></a><span data-ttu-id="8f184-144">\_ \_ máquina local del almacén del sistema \_ CERT \_</span><span class="sxs-lookup"><span data-stu-id="8f184-144">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>

<span data-ttu-id="8f184-145">\_ \_ \_ Los almacenes del sistema del equipo local del almacén del sistema \_ de certificados se encuentran en la siguiente ubicación del registro:</span><span class="sxs-lookup"><span data-stu-id="8f184-145">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         SystemCertificates
```

<span data-ttu-id="8f184-146">Los almacenes físicos predefinidos se asocian a los almacenes del sistema como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="8f184-146">The predefined physical stores are associated with those system stores are as follows.</span></span>



| <span data-ttu-id="8f184-147">Almacén del sistema</span><span class="sxs-lookup"><span data-stu-id="8f184-147">System store</span></span> | <span data-ttu-id="8f184-148">Almacén físico</span><span class="sxs-lookup"><span data-stu-id="8f184-148">Physical store</span></span>                                                                                    |
|--------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f184-149">MY</span><span class="sxs-lookup"><span data-stu-id="8f184-149">MY</span></span>           | <span data-ttu-id="8f184-150">. Predeterminada</span><span class="sxs-lookup"><span data-stu-id="8f184-150">.Default</span></span>                                                                                          |
| <span data-ttu-id="8f184-151">Root</span><span class="sxs-lookup"><span data-stu-id="8f184-151">Root</span></span>         | <span data-ttu-id="8f184-152">. Default. AuthRoot</span><span class="sxs-lookup"><span data-stu-id="8f184-152">.Default.AuthRoot</span></span><br/> <span data-ttu-id="8f184-153">. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="8f184-153">.GroupPolicy</span></span><br/> <span data-ttu-id="8f184-154">. Entidades</span><span class="sxs-lookup"><span data-stu-id="8f184-154">.Enterprise</span></span><br/> <span data-ttu-id="8f184-155">. Tarjeta</span><span class="sxs-lookup"><span data-stu-id="8f184-155">.SmartCard</span></span><br/> |
| <span data-ttu-id="8f184-156">Confianza</span><span class="sxs-lookup"><span data-stu-id="8f184-156">Trust</span></span>        | <span data-ttu-id="8f184-157">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="8f184-157">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="8f184-158">. Entidades</span><span class="sxs-lookup"><span data-stu-id="8f184-158">.Enterprise</span></span><br/>                                            |
| <span data-ttu-id="8f184-159">CA</span><span class="sxs-lookup"><span data-stu-id="8f184-159">CA</span></span>           | <span data-ttu-id="8f184-160">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="8f184-160">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="8f184-161">. Entidades</span><span class="sxs-lookup"><span data-stu-id="8f184-161">.Enterprise</span></span> <br/>                                           |



 

### <a name="cert_system_store_current_service"></a><span data-ttu-id="8f184-162">\_ \_ servicio actual del almacén del sistema \_ de certificados \_</span><span class="sxs-lookup"><span data-stu-id="8f184-162">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE</span></span>

<span data-ttu-id="8f184-163">\_ \_ \_ \_ Los almacenes del sistema del servicio del almacén del sistema de certificados se encuentran en la siguiente ubicación del registro:</span><span class="sxs-lookup"><span data-stu-id="8f184-163">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

<span data-ttu-id="8f184-164">Los almacenes físicos predefinidos asociados a esos almacenes del sistema son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="8f184-164">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="8f184-165">Almacén del sistema</span><span class="sxs-lookup"><span data-stu-id="8f184-165">System store</span></span> | <span data-ttu-id="8f184-166">Almacén físico</span><span class="sxs-lookup"><span data-stu-id="8f184-166">Physical store</span></span>                   |
|--------------|----------------------------------|
| <span data-ttu-id="8f184-167">MY</span><span class="sxs-lookup"><span data-stu-id="8f184-167">MY</span></span>           | <span data-ttu-id="8f184-168">. Predeterminada</span><span class="sxs-lookup"><span data-stu-id="8f184-168">.Default</span></span>                         |
| <span data-ttu-id="8f184-169">Root</span><span class="sxs-lookup"><span data-stu-id="8f184-169">Root</span></span>         | <span data-ttu-id="8f184-170">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="8f184-170">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="8f184-171">Confianza</span><span class="sxs-lookup"><span data-stu-id="8f184-171">Trust</span></span>        | <span data-ttu-id="8f184-172">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="8f184-172">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="8f184-173">CA</span><span class="sxs-lookup"><span data-stu-id="8f184-173">CA</span></span>           | <span data-ttu-id="8f184-174">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="8f184-174">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_store_services"></a><span data-ttu-id="8f184-175">\_servicios del \_ almacén del sistema de certificados \_</span><span class="sxs-lookup"><span data-stu-id="8f184-175">CERT\_SYSTEM\_STORE\_SERVICES</span></span>

<span data-ttu-id="8f184-176">\_ \_ Los almacenes del sistema de certificados del almacén del sistema \_ se encuentran en la siguiente ubicación del registro:</span><span class="sxs-lookup"><span data-stu-id="8f184-176">CERT\_SYSTEM\_STORE\_SERVICES system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

<span data-ttu-id="8f184-177">Los almacenes físicos predefinidos asociados a esos almacenes del sistema son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="8f184-177">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="8f184-178">Almacén del sistema</span><span class="sxs-lookup"><span data-stu-id="8f184-178">System store</span></span>       | <span data-ttu-id="8f184-179">Almacén físico</span><span class="sxs-lookup"><span data-stu-id="8f184-179">Physical store</span></span>                   |
|--------------------|----------------------------------|
| <span data-ttu-id="8f184-180">ServiceName \\ mi</span><span class="sxs-lookup"><span data-stu-id="8f184-180">ServiceName\\MY</span></span>    | <span data-ttu-id="8f184-181">. Predeterminada</span><span class="sxs-lookup"><span data-stu-id="8f184-181">.Default</span></span>                         |
| <span data-ttu-id="8f184-182">ServiceName \\ raíz</span><span class="sxs-lookup"><span data-stu-id="8f184-182">ServiceName\\Root</span></span>  | <span data-ttu-id="8f184-183">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="8f184-183">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="8f184-184">ServiceName \\ confianza</span><span class="sxs-lookup"><span data-stu-id="8f184-184">ServiceName\\Trust</span></span> | <span data-ttu-id="8f184-185">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="8f184-185">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="8f184-186">\\CA ServiceName</span><span class="sxs-lookup"><span data-stu-id="8f184-186">ServiceName\\CA</span></span>    | <span data-ttu-id="8f184-187">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="8f184-187">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_store_users"></a><span data-ttu-id="8f184-188">\_usuarios del \_ almacén del sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="8f184-188">CERT\_SYSTEM\_STORE\_USERS</span></span>

<span data-ttu-id="8f184-189">\_ \_ \_ Los almacenes del sistema del almacén del sistema de certificados se encuentran en la siguiente ubicación del registro:</span><span class="sxs-lookup"><span data-stu-id="8f184-189">CERT\_SYSTEM\_STORE\_USERS system stores are at the following registry location:</span></span>

```
HKEY_USERS
   UserName
      Software
         Microsoft
            SystemCertificates
```

<span data-ttu-id="8f184-190">Los almacenes físicos predefinidos asociados a esos almacenes del sistema son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="8f184-190">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="8f184-191">Almacén del sistema</span><span class="sxs-lookup"><span data-stu-id="8f184-191">System store</span></span>  | <span data-ttu-id="8f184-192">Almacén físico</span><span class="sxs-lookup"><span data-stu-id="8f184-192">Physical store</span></span>                   |
|---------------|----------------------------------|
| <span data-ttu-id="8f184-193">userid \\ My</span><span class="sxs-lookup"><span data-stu-id="8f184-193">userid\\MY</span></span>    | <span data-ttu-id="8f184-194">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="8f184-194">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="8f184-195">userid \\ raíz</span><span class="sxs-lookup"><span data-stu-id="8f184-195">userid\\Root</span></span>  | <span data-ttu-id="8f184-196">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="8f184-196">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="8f184-197">userid \\ confianza</span><span class="sxs-lookup"><span data-stu-id="8f184-197">userid\\Trust</span></span> | <span data-ttu-id="8f184-198">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="8f184-198">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="8f184-199">userid \\ CA</span><span class="sxs-lookup"><span data-stu-id="8f184-199">userid\\CA</span></span>    | <span data-ttu-id="8f184-200">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="8f184-200">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_current_user_group_policy"></a><span data-ttu-id="8f184-201">\_Directiva de \_ \_ grupo de usuario actual del \_ sistema \_ de certificados</span><span class="sxs-lookup"><span data-stu-id="8f184-201">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY</span></span>

<span data-ttu-id="8f184-202">\_ \_ \_ \_ \_ Los almacenes del sistema de la Directiva de grupo del usuario actual del sistema de certificados se encuentran en la siguiente ubicación del registro:</span><span class="sxs-lookup"><span data-stu-id="8f184-202">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY system stores are at the following registry location:</span></span>

```
HKEY_CURRENT_USER
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_local_machine_group_policy"></a><span data-ttu-id="8f184-203">\_Directiva de \_ \_ Grupo del equipo local \_ \_ del sistema de certificados</span><span class="sxs-lookup"><span data-stu-id="8f184-203">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>

<span data-ttu-id="8f184-204">\_ \_ \_ \_ \_ Los almacenes del sistema de la Directiva de grupo del equipo local del sistema de certificados se encuentran en la siguiente ubicación del registro:</span><span class="sxs-lookup"><span data-stu-id="8f184-204">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_store_local_machine_enterprise"></a><span data-ttu-id="8f184-205">certificado de la \_ \_ \_ máquina local del almacén \_ del sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="8f184-205">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE</span></span>

<span data-ttu-id="8f184-206">\_Almacén del sistema de certificados: la \_ \_ \_ máquina local \_ contiene los certificados compartidos entre dominios de la empresa y descargados del directorio global de la empresa.</span><span class="sxs-lookup"><span data-stu-id="8f184-206">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE contains certificates shared across domains in the enterprise and downloaded from the global enterprise directory.</span></span> <span data-ttu-id="8f184-207">Para sincronizar el almacén empresarial del cliente, el directorio empresarial se sondea cada ocho horas y los certificados se descargan automáticamente en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="8f184-207">To synchronize the client's enterprise store, the enterprise directory is polled every eight hours and certificates are downloaded automatically in the background.</span></span>

<span data-ttu-id="8f184-208">Los almacenes físicos predefinidos asociados a estos almacenes del sistema son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="8f184-208">The predefined physical stores associated with these system stores are as follows.</span></span>



| <span data-ttu-id="8f184-209">Almacén del sistema</span><span class="sxs-lookup"><span data-stu-id="8f184-209">System store</span></span> | <span data-ttu-id="8f184-210">Almacén físico</span><span class="sxs-lookup"><span data-stu-id="8f184-210">Physical store</span></span> |
|--------------|----------------|
| <span data-ttu-id="8f184-211">MY</span><span class="sxs-lookup"><span data-stu-id="8f184-211">MY</span></span>           | <span data-ttu-id="8f184-212">. Predeterminada</span><span class="sxs-lookup"><span data-stu-id="8f184-212">.Default</span></span>       |
| <span data-ttu-id="8f184-213">Root</span><span class="sxs-lookup"><span data-stu-id="8f184-213">Root</span></span>         | <span data-ttu-id="8f184-214">. Predeterminada</span><span class="sxs-lookup"><span data-stu-id="8f184-214">.Default</span></span>       |
| <span data-ttu-id="8f184-215">Confianza</span><span class="sxs-lookup"><span data-stu-id="8f184-215">Trust</span></span>        | <span data-ttu-id="8f184-216">. Predeterminada</span><span class="sxs-lookup"><span data-stu-id="8f184-216">.Default</span></span>       |
| <span data-ttu-id="8f184-217">CA</span><span class="sxs-lookup"><span data-stu-id="8f184-217">CA</span></span>           | <span data-ttu-id="8f184-218">. Predeterminada</span><span class="sxs-lookup"><span data-stu-id="8f184-218">.Default</span></span>       |



 

### <a name="remarks"></a><span data-ttu-id="8f184-219">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f184-219">Remarks</span></span>

<span data-ttu-id="8f184-220">Se pueden asociar almacenes físicos adicionales a un almacén del sistema mediante [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).</span><span class="sxs-lookup"><span data-stu-id="8f184-220">Additional physical stores can be associated with a system store by using [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).</span></span>

<span data-ttu-id="8f184-221">\_ \_ Los almacenes de certificados \_ de servicio de almacén de sistema y certificado \_ de almacén del sistema \_ de certificados \_ se abren prefijando el nombre del almacén en la cadena que se pasa a *pvPara* con el nombre de servicio o de usuario como *ServiceName* \\ **Trust** o **.** \\ **Mi**.</span><span class="sxs-lookup"><span data-stu-id="8f184-221">CERT\_SYSTEM\_STORE\_SERVICE and CERT\_SYSTEM\_STORE\_USERS stores are opened by prefixing the name of the store in the string passed to *pvPara* with the service or user name such as *ServiceName*\\**Trust** or **.Default**\\**MY**.</span></span> <span data-ttu-id="8f184-222">La ubicación de los usuarios de los servicios del almacén del sistema de certificados \_ \_ o del \_ \_ almacén del sistema \_ de certificados \_ puede abrir el mismo almacén en el \_ servicio actual del sistema de certificados \_ o el \_ \_ usuario actual del almacén del sistema de certificados mediante \_ \_ \_ el [*identificador de seguridad*](../secgloss/s-gly.md) de texto (SID) del servicio o usuario actual.</span><span class="sxs-lookup"><span data-stu-id="8f184-222">The CERT\_SYSTEM\_STORE\_SERVICES or CERT\_SYSTEM\_STORE\_USERS location can open the same store in CERT\_SYSTEM\_CURRENT\_SERVICE or CERT\_SYSTEM\_STORE\_CURRENT\_USER by using the textual [*security identifier*](../secgloss/s-gly.md) (SID) of the current service or user.</span></span>

<span data-ttu-id="8f184-223">Los almacenes de \_ la Directiva de grupo de usuarios del almacén del sistema de certificados \_ \_ \_ \_ y \_ \_ \_ la Directiva de grupo del equipo local del sistema de certificados \_ \_ en una configuración de red se descargan en el equipo cliente desde la plantilla de directiva de grupo (GPT) durante el inicio del equipo o el inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="8f184-223">Stores in CERT\_SYSTEM\_STORE\_USER\_GROUP\_POLICY and CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY in a network setting are downloaded to the client computer from the Group Policy Template (GPT) during computer startup or user logon.</span></span> <span data-ttu-id="8f184-224">Estos almacenes se pueden actualizar en el equipo cliente después del inicio o el inicio de sesión cuando un administrador cambia la GPT en el servidor de dominio.</span><span class="sxs-lookup"><span data-stu-id="8f184-224">These stores can be updated on the client computer after startup or logon when the GPT is changed on the domain server by an administrator.</span></span> <span data-ttu-id="8f184-225">La función [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) permite a una aplicación recibir una notificación cuando los almacenes en cualquiera de estas ubicaciones han cambiado.</span><span class="sxs-lookup"><span data-stu-id="8f184-225">The [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) function allows an application to be notified when stores in either of these locations have changed.</span></span>

<span data-ttu-id="8f184-226">Las siguientes ubicaciones del almacén del sistema se pueden abrir de forma remota:</span><span class="sxs-lookup"><span data-stu-id="8f184-226">The following system store locations can be opened remotely:</span></span>

-   <span data-ttu-id="8f184-227">\_ \_ máquina local del almacén del sistema \_ CERT \_</span><span class="sxs-lookup"><span data-stu-id="8f184-227">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>
-   <span data-ttu-id="8f184-228">\_Directiva de \_ \_ Grupo del \_ equipo local del \_ almacén \_ del sistema de certificados</span><span class="sxs-lookup"><span data-stu-id="8f184-228">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>
-   <span data-ttu-id="8f184-229">\_servicios del \_ almacén del sistema de certificados \_</span><span class="sxs-lookup"><span data-stu-id="8f184-229">CERT\_SYSTEM\_STORE\_SERVICES</span></span>
-   <span data-ttu-id="8f184-230">\_usuarios del \_ almacén del sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="8f184-230">CERT\_SYSTEM\_STORE\_USERS</span></span>

<span data-ttu-id="8f184-231">Las ubicaciones del almacén del sistema se abren de forma remota mediante el prefijo del nombre del almacén en la cadena que se pasa a *pvPara* con el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="8f184-231">System store locations are opened remotely by prefixing the store name in the string passed to *pvPara* with the computer name.</span></span> <span data-ttu-id="8f184-232">Ejemplos de nombres de almacén del sistema remoto:</span><span class="sxs-lookup"><span data-stu-id="8f184-232">Examples of remote system store names are:</span></span>

-   <span data-ttu-id="8f184-233">*Nombre del equipo* \\ **Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="8f184-233">*ComputerName*\\**CA**</span></span>
-   <span data-ttu-id="8f184-234">\\\\*Nombre del equipo* \\ **Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="8f184-234">\\\\*ComputerName*\\**CA**</span></span>
-   <span data-ttu-id="8f184-235">*Nombre del equipo* \\ *ServiceName* \\ **Confianza** de</span><span class="sxs-lookup"><span data-stu-id="8f184-235">*ComputerName*\\*ServiceName*\\**Trust**</span></span>
-   <span data-ttu-id="8f184-236">\\\\*Nombre del equipo* \\ *ServiceName* \\ **Confianza** de</span><span class="sxs-lookup"><span data-stu-id="8f184-236">\\\\*ComputerName*\\*ServiceName*\\**Trust**</span></span>

 

 
