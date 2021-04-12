---
description: Una infraestructura de clave pública (PKI) de Windows guarda los certificados en el servidor que hospeda la entidad de certificación (CA) y en el equipo o dispositivo local.
ms.assetid: b6aaafeb-30d1-453e-a70c-dcaa01fea1cf
title: Directorio de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee525e4d910de1c75516c6aaa27ca41a6cfa17c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279472"
---
# <a name="certificate-directory"></a><span data-ttu-id="1e834-103">Directorio de certificados</span><span class="sxs-lookup"><span data-stu-id="1e834-103">Certificate Directory</span></span>

<span data-ttu-id="1e834-104">Una infraestructura de clave pública (PKI) de Windows guarda los certificados en el servidor que hospeda la entidad de certificación (CA) y en el equipo o dispositivo local.</span><span class="sxs-lookup"><span data-stu-id="1e834-104">A Windows public key infrastructure (PKI) saves certificates on the server that hosts the certification authority (CA) and on the local computer or device.</span></span> <span data-ttu-id="1e834-105">Normalmente, el almacenamiento de CA se conoce como la base de datos de certificados y el almacenamiento local se conoce como el almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="1e834-105">CA storage is typically referred to as the certificate database, and local storage is known as the certificate store.</span></span>

## <a name="certificate-database"></a><span data-ttu-id="1e834-106">Base de datos de certificados</span><span class="sxs-lookup"><span data-stu-id="1e834-106">Certificate Database</span></span>

<span data-ttu-id="1e834-107">Al agregar servicios de servidor de certificados en un servidor de Windows y configurar una CA, se crea una base de datos de certificados.</span><span class="sxs-lookup"><span data-stu-id="1e834-107">When you add Certificate Services on a Windows server and configure a CA, a certificate database is created.</span></span> <span data-ttu-id="1e834-108">De forma predeterminada, la base de datos se encuentra en la carpeta *% systemroot%* \\ system32 \\ Certlog y el nombre se basa en el nombre de la entidad de certificación con una extensión. edb.</span><span class="sxs-lookup"><span data-stu-id="1e834-108">By default, the database is contained in the *%SystemRoot%*\\System32\\Certlog folder, and the name is based on the CA name with an .edb extension.</span></span> <span data-ttu-id="1e834-109">La base de datos puede contener:</span><span class="sxs-lookup"><span data-stu-id="1e834-109">The database can contain:</span></span>

-   <span data-ttu-id="1e834-110">Certificados emitidos</span><span class="sxs-lookup"><span data-stu-id="1e834-110">Issued certificates</span></span>
-   <span data-ttu-id="1e834-111">Certificados revocados</span><span class="sxs-lookup"><span data-stu-id="1e834-111">Revoked certificates</span></span>
-   <span data-ttu-id="1e834-112">Claves privadas archivadas</span><span class="sxs-lookup"><span data-stu-id="1e834-112">Archived private keys</span></span>
-   <span data-ttu-id="1e834-113">Solicitudes de certificado</span><span class="sxs-lookup"><span data-stu-id="1e834-113">Certificate requests</span></span>

<span data-ttu-id="1e834-114">No se puede usar la API de inscripción de certificados para manipular la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1e834-114">You cannot use the Certificate Enrollment API to manipulate the database.</span></span> <span data-ttu-id="1e834-115">El proceso de inscripción crea automáticamente las entradas necesarias.</span><span class="sxs-lookup"><span data-stu-id="1e834-115">The enrollment process automatically creates the necessary entries.</span></span>

## <a name="certificate-stores"></a><span data-ttu-id="1e834-116">Almacenes de certificados</span><span class="sxs-lookup"><span data-stu-id="1e834-116">Certificate Stores</span></span>

<span data-ttu-id="1e834-117">Servicios de certificados de Microsoft copia los certificados emitidos y las solicitudes pendientes o rechazadas a los equipos y dispositivos locales.</span><span class="sxs-lookup"><span data-stu-id="1e834-117">Microsoft Certificate Services copies issued certificates and pending or rejected requests to local computers and devices.</span></span> <span data-ttu-id="1e834-118">La ubicación de almacenamiento se denomina almacén de certificados y consta de los siguientes almacenes lógicos.</span><span class="sxs-lookup"><span data-stu-id="1e834-118">The storage location is called the certificate store and consists of the following logical stores.</span></span>

| <span data-ttu-id="1e834-119">Almacén lógico</span><span class="sxs-lookup"><span data-stu-id="1e834-119">Logical store</span></span>                                         | <span data-ttu-id="1e834-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e834-120">Description</span></span>                                                                                                            |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e834-121">Personal</span><span class="sxs-lookup"><span data-stu-id="1e834-121">Personal</span></span><br/>                                   | <span data-ttu-id="1e834-122">Contiene certificados asociados a una clave privada controlada por el usuario o el equipo.</span><span class="sxs-lookup"><span data-stu-id="1e834-122">Contains certificates associated with a private key controlled by the user or computer.</span></span><br/>                     |
| <span data-ttu-id="1e834-123">Entidades de certificación raíz de confianza</span><span class="sxs-lookup"><span data-stu-id="1e834-123">Trusted Root Certification Authorities</span></span><br/>     | <span data-ttu-id="1e834-124">Contiene certificados de entidades de certificación (CA) de confianza implícita.</span><span class="sxs-lookup"><span data-stu-id="1e834-124">Contains certificates from implicitly trusted certification authorities (CAs).</span></span><br/>                              |
| <span data-ttu-id="1e834-125">Confianza empresarial</span><span class="sxs-lookup"><span data-stu-id="1e834-125">Enterprise Trust</span></span><br/>                           | <span data-ttu-id="1e834-126">Contiene listas de certificados de confianza que se suelen usar para confiar en los certificados autofirmados de otras organizaciones.</span><span class="sxs-lookup"><span data-stu-id="1e834-126">Contains certificate trust lists typically used to trust self-signed certificates from other organizations.</span></span><br/> |
| <span data-ttu-id="1e834-127">Entidades de certificación intermedias</span><span class="sxs-lookup"><span data-stu-id="1e834-127">Intermediate Certification Authorities</span></span><br/>     | <span data-ttu-id="1e834-128">Contiene certificados emitidos para entidades de certificación subordinadas en la jerarquía de certificados.</span><span class="sxs-lookup"><span data-stu-id="1e834-128">Contains certificates issued to subordinate CAs in the certification hierarchy.</span></span><br/>                             |
| <span data-ttu-id="1e834-129">Objeto de usuario de Active Directory</span><span class="sxs-lookup"><span data-stu-id="1e834-129">Active Directory User Object</span></span><br/>               | <span data-ttu-id="1e834-130">Contiene el certificado de objeto de usuario o los certificados publicados en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1e834-130">Contains the user object certificate or certificates published in Active Directory.</span></span><br/>                         |
| <span data-ttu-id="1e834-131">Publicadores de confianza</span><span class="sxs-lookup"><span data-stu-id="1e834-131">Trusted Publishers</span></span><br/>                         | <span data-ttu-id="1e834-132">Contiene certificados de entidades de certificación de confianza.</span><span class="sxs-lookup"><span data-stu-id="1e834-132">Contains certificates from trusted CAs.</span></span><br/>                                                                     |
| <span data-ttu-id="1e834-133">Certificados que no son de confianza</span><span class="sxs-lookup"><span data-stu-id="1e834-133">Untrusted Certificates</span></span><br/>                     | <span data-ttu-id="1e834-134">Contiene certificados que se han identificado explícitamente como que no son de confianza.</span><span class="sxs-lookup"><span data-stu-id="1e834-134">Contains certificates that have been explicitly identified as untrusted.</span></span><br/>                                    |
| <span data-ttu-id="1e834-135">Entidades de certificación raíz de tercero</span><span class="sxs-lookup"><span data-stu-id="1e834-135">Third-Party Root Certification Authorities</span></span><br/> | <span data-ttu-id="1e834-136">Contiene certificados raíz de confianza de entidades de certificación fuera de la jerarquía interna de certificados.</span><span class="sxs-lookup"><span data-stu-id="1e834-136">Contains trusted root certificates from CAs outside the internal certificate hierarchy.</span></span><br/>                     |
| <span data-ttu-id="1e834-137">Personas de confianza</span><span class="sxs-lookup"><span data-stu-id="1e834-137">Trusted People</span></span><br/>                             | <span data-ttu-id="1e834-138">Contiene certificados emitidos para usuarios o entidades de confianza explícita.</span><span class="sxs-lookup"><span data-stu-id="1e834-138">Contains certificates issued to users or entities that have been explicitly trusted.</span></span><br/>                        |
| <span data-ttu-id="1e834-139">Otras personas</span><span class="sxs-lookup"><span data-stu-id="1e834-139">Other People</span></span><br/>                               | <span data-ttu-id="1e834-140">Contiene certificados emitidos para usuarios o entidades de confianza implícita.</span><span class="sxs-lookup"><span data-stu-id="1e834-140">Contains certificates issued to users or entities that have been implicitly trusted.</span></span><br/>                        |
| <span data-ttu-id="1e834-141">Solicitudes de inscripción de certificado</span><span class="sxs-lookup"><span data-stu-id="1e834-141">Certificate Enrollment Requests</span></span><br/>            | <span data-ttu-id="1e834-142">Contiene solicitudes de certificados pendientes o rechazadas.</span><span class="sxs-lookup"><span data-stu-id="1e834-142">Contains pending or rejected certificate requests.</span></span><br/>                                                          |



 

<span data-ttu-id="1e834-143">No se puede usar la API de inscripción de certificados para especificar o recuperar propiedades de almacén o para copiar certificados en almacenes específicos.</span><span class="sxs-lookup"><span data-stu-id="1e834-143">You cannot use the Certificate Enrollment API to specify or retrieve store properties or copy certificates to specific stores.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e834-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1e834-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e834-145">Elementos PKI</span><span class="sxs-lookup"><span data-stu-id="1e834-145">PKI Elements</span></span>](about-pki-components.md)
</dt> </dl>

 

 




