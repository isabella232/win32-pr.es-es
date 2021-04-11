---
description: Durante la actualización de un equipo o una migración de equipo a equipo, se migrarán los certificados de determinados almacenes de certificados.
ms.assetid: fe81d578-f2f6-41f0-9ebf-e7bd5532bed9
title: Migración del almacén de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31b42b83718aa1cab786ad79cc2df754b8fd9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083143"
---
# <a name="certificate-store-migration"></a><span data-ttu-id="2f589-103">Migración del almacén de certificados</span><span class="sxs-lookup"><span data-stu-id="2f589-103">Certificate Store Migration</span></span>

<span data-ttu-id="2f589-104">Durante la actualización de un equipo o una migración de equipo a equipo, se migrarán los certificados de determinados almacenes de certificados.</span><span class="sxs-lookup"><span data-stu-id="2f589-104">During a computer upgrade or a computer-to-computer migration, the certificates in certain certificate stores will be migrated.</span></span> <span data-ttu-id="2f589-105">En la tabla siguiente se enumeran los almacenes de certificados que se migran de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2f589-105">The following table lists the certificate stores that are migrated by default.</span></span> <span data-ttu-id="2f589-106">En el almacén configuración de la solicitud de certificados automática (ACRS) del sistema, solo se migran las [*listas de certificados de confianza*](../secgloss/c-gly.md) (CTL).</span><span class="sxs-lookup"><span data-stu-id="2f589-106">For the system Automatic Certificate Request Settings (ACRS) store, only the [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) are migrated.</span></span> <span data-ttu-id="2f589-107">En el resto de almacenes que se enumeran a continuación, solo se migran los certificados.</span><span class="sxs-lookup"><span data-stu-id="2f589-107">For all other stores listed below, only the certificates are migrated.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2f589-108">Sistema/usuario</span><span class="sxs-lookup"><span data-stu-id="2f589-108">System/user</span></span></th>
<th><span data-ttu-id="2f589-109">Tienda</span><span class="sxs-lookup"><span data-stu-id="2f589-109">Store</span></span></th>
<th><span data-ttu-id="2f589-110">Ubicación de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="2f589-110">Storage location</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2f589-111">$ {ROWSPAN8} $System $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="2f589-111">${ROWSPAN8}$System${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="2f589-112">ROOT</span><span class="sxs-lookup"><span data-stu-id="2f589-112">ROOT</span></span></td>
<td><span data-ttu-id="2f589-113"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Raíz</strong> \ de <strong>Certificados</strong> de</span><span class="sxs-lookup"><span data-stu-id="2f589-113"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Root</strong>\<strong>Certificates</strong></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f589-114">MY</span><span class="sxs-lookup"><span data-stu-id="2f589-114">MY</span></span></td>
<td><span data-ttu-id="2f589-115"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Mi</strong> \ <strong>Certificados</strong> de</span><span class="sxs-lookup"><span data-stu-id="2f589-115"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>My</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="2f589-116">Solicite</span><span class="sxs-lookup"><span data-stu-id="2f589-116">REQUEST</span></span></td>
<td><span data-ttu-id="2f589-117"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Solicitud</strong> \ de <strong>Certificados</strong> de</span><span class="sxs-lookup"><span data-stu-id="2f589-117"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Request</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="2f589-118">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="2f589-118">TrustedPublisher</span></span></td>
<td><span data-ttu-id="2f589-119"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificados</strong> de</span><span class="sxs-lookup"><span data-stu-id="2f589-119"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPublisher</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="2f589-120">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="2f589-120">TrustedPeople</span></span></td>
<td><span data-ttu-id="2f589-121"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificados</strong> de</span><span class="sxs-lookup"><span data-stu-id="2f589-121"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPeople</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="2f589-122">No permitida.</span><span class="sxs-lookup"><span data-stu-id="2f589-122">Disallowed</span></span></td>
<td><span data-ttu-id="2f589-123"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ No <strong>permitido</strong> \ <strong>Certificados</strong> de</span><span class="sxs-lookup"><span data-stu-id="2f589-123"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Disallowed</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="2f589-124">CA</span><span class="sxs-lookup"><span data-stu-id="2f589-124">CA</span></span></td>
<td><span data-ttu-id="2f589-125"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Entidad de certificación</strong> \ <strong>Certificados</strong> de</span><span class="sxs-lookup"><span data-stu-id="2f589-125"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>CA</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="2f589-126">ACR</span><span class="sxs-lookup"><span data-stu-id="2f589-126">ACRS</span></span></td>
<td><span data-ttu-id="2f589-127"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>ACRS</strong> \ <strong>CTL</strong></span><span class="sxs-lookup"><span data-stu-id="2f589-127"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>ACRS</strong>\<strong>CTLs</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td rowspan="7"><span data-ttu-id="2f589-128">Usuario $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="2f589-128">User${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="2f589-129">ROOT</span><span class="sxs-lookup"><span data-stu-id="2f589-129">ROOT</span></span></td>
<td><span data-ttu-id="2f589-130"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Raíz</strong> \ de <strong>Certificados</strong> de</span><span class="sxs-lookup"><span data-stu-id="2f589-130"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Root</strong>\<strong>Certificates</strong></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f589-131">MY</span><span class="sxs-lookup"><span data-stu-id="2f589-131">MY</span></span></td>
<td><span data-ttu-id="2f589-132">archivo: \\ %AppData%\Microsoft\SystemCertificates\My\Certificates</span><span class="sxs-lookup"><span data-stu-id="2f589-132">file:\\%APPDATA%\Microsoft\SystemCertificates\My\Certificates</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="2f589-133">Solicite</span><span class="sxs-lookup"><span data-stu-id="2f589-133">REQUEST</span></span></td>
<td><span data-ttu-id="2f589-134">archivo: \\ %AppData%\Microsoft\SystemCertificates\Request\Certificates</span><span class="sxs-lookup"><span data-stu-id="2f589-134">file:\\%APPDATA%\Microsoft\SystemCertificates\Request\Certificates</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="2f589-135">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="2f589-135">TrustedPublisher</span></span></td>
<td><span data-ttu-id="2f589-136"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificados</strong> de</span><span class="sxs-lookup"><span data-stu-id="2f589-136"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPublisher</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="2f589-137">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="2f589-137">TrustedPeople</span></span></td>
<td><span data-ttu-id="2f589-138"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificados</strong> de</span><span class="sxs-lookup"><span data-stu-id="2f589-138"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPeople</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="2f589-139">No permitida.</span><span class="sxs-lookup"><span data-stu-id="2f589-139">Disallowed</span></span></td>
<td><span data-ttu-id="2f589-140"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ No <strong>permitido</strong> \ <strong>Certificados</strong> de</span><span class="sxs-lookup"><span data-stu-id="2f589-140"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Disallowed</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="2f589-141">CA</span><span class="sxs-lookup"><span data-stu-id="2f589-141">CA</span></span></td>
<td><span data-ttu-id="2f589-142"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Entidad de certificación</strong> \ <strong>Certificados</strong> de</span><span class="sxs-lookup"><span data-stu-id="2f589-142"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>CA</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="2f589-143">Otros almacenes de certificados creados por aplicaciones no se migran de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2f589-143">Other certificate stores created by applications are not migrated by default.</span></span> <span data-ttu-id="2f589-144">Las aplicaciones que crean sus propias tiendas son responsables de la migración de los almacenes que crean.</span><span class="sxs-lookup"><span data-stu-id="2f589-144">Applications that create their own stores are responsible for migration of the stores that they create.</span></span> <span data-ttu-id="2f589-145">Para crear almacenes, se recomienda que defina una clave del registro en la configuración de la aplicación y que cree un almacén dentro de la configuración del registro mediante el proveedor de almacenamiento de **\_ Prov. \_ \_ reg del almacén de certificados** .</span><span class="sxs-lookup"><span data-stu-id="2f589-145">To create stores, we recommend that you define a registry key in the application settings and create a store within the registry settings by using the **CERT\_STORE\_PROV\_REG** store provider.</span></span> <span data-ttu-id="2f589-146">Para obtener más información acerca de cómo migrar la configuración de la aplicación, consulte el tema *How to Create a Custom. xml file* en la guía *using USMT 3,0* en [herramienta de migración de estado de usuario 3,0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx).</span><span class="sxs-lookup"><span data-stu-id="2f589-146">For more information about migrating application settings, see the *How To Create a Custom .xml File* topic in the *Using USMT 3.0* guide at [User State Migration Tool 3.0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx).</span></span> <span data-ttu-id="2f589-147">(Es posible que este recurso no esté disponible en algunos idiomas y países o regiones).</span><span class="sxs-lookup"><span data-stu-id="2f589-147">(This resource may not be available in some languages and countries or regions.)</span></span>

 

 
