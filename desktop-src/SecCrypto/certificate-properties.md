---
description: Servicios de Certificate Server admite el uso de certificados tal y como se define en la recomendación X. 509 de ITU-T (también ISO/IEC 9594-8).
ms.assetid: 59f20de0-de24-43c7-a1a2-bdc91ee28059
title: Propiedades del certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc234f574e0b5bef2d4884706584b5c33ea9c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908981"
---
# <a name="certificate-properties"></a><span data-ttu-id="b4794-103">Propiedades del certificado</span><span class="sxs-lookup"><span data-stu-id="b4794-103">Certificate Properties</span></span>

<span data-ttu-id="b4794-104">Servicios de Certificate Server admite el uso de certificados tal y como se define en la recomendación [*X. 509*](../secgloss/x-gly.md) de ITU-T (también ISO/IEC 9594-8).</span><span class="sxs-lookup"><span data-stu-id="b4794-104">Certificate Services supports the use of certificates as defined in the ITU-T recommendation [*X.509*](../secgloss/x-gly.md) (also, ISO/IEC 9594-8).</span></span> <span data-ttu-id="b4794-105">A continuación se muestran las propiedades contenidas en un certificado X. 509 estándar.</span><span class="sxs-lookup"><span data-stu-id="b4794-105">The following are properties that are contained in a standard X.509 certificate.</span></span>



| <span data-ttu-id="b4794-106">Campo</span><span class="sxs-lookup"><span data-stu-id="b4794-106">Field</span></span>                                       | <span data-ttu-id="b4794-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4794-107">Description</span></span>                                                                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4794-108">Versión</span><span class="sxs-lookup"><span data-stu-id="b4794-108">Version</span></span>                                     | <span data-ttu-id="b4794-109">Número de versión del formato de certificado.</span><span class="sxs-lookup"><span data-stu-id="b4794-109">Version number of the certificate format.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="b4794-110">Número de serie</span><span class="sxs-lookup"><span data-stu-id="b4794-110">Serial Number</span></span>                               | <span data-ttu-id="b4794-111">Número de serie del certificado.</span><span class="sxs-lookup"><span data-stu-id="b4794-111">Serial number of the certificate.</span></span> <span data-ttu-id="b4794-112">Este número lo asigna el emisor y es único en la lista de certificados emitidos del emisor.</span><span class="sxs-lookup"><span data-stu-id="b4794-112">This number is assigned by the issuer and is unique within the issuer's list of issued certificates.</span></span>                                                                          |
| <span data-ttu-id="b4794-113">Identificador y parámetros de algoritmo</span><span class="sxs-lookup"><span data-stu-id="b4794-113">Algorithm Identifier and Parameters</span></span>         | <span data-ttu-id="b4794-114">Algoritmo de firma y cualquier parámetro utilizado por el emisor.</span><span class="sxs-lookup"><span data-stu-id="b4794-114">Signature algorithm and any parameters used by the issuer.</span></span>                                                                                                                                                      |
| <span data-ttu-id="b4794-115">Emisor</span><span class="sxs-lookup"><span data-stu-id="b4794-115">Issuer</span></span>                                      | <span data-ttu-id="b4794-116">Nombre de la [*entidad de certificación*](../secgloss/c-gly.md) que emitió el certificado.</span><span class="sxs-lookup"><span data-stu-id="b4794-116">Name of the [*certification authority*](../secgloss/c-gly.md) which issued the certificate.</span></span>                                               |
| <span data-ttu-id="b4794-117">No antes de (fecha)</span><span class="sxs-lookup"><span data-stu-id="b4794-117">Not Before (Date)</span></span>                           | <span data-ttu-id="b4794-118">Certificado no válido antes de esta fecha.</span><span class="sxs-lookup"><span data-stu-id="b4794-118">Certificate not valid before this date.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="b4794-119">No después de (fecha)</span><span class="sxs-lookup"><span data-stu-id="b4794-119">Not After (Date)</span></span>                            | <span data-ttu-id="b4794-120">Certificado no válido después de esta fecha.</span><span class="sxs-lookup"><span data-stu-id="b4794-120">Certificate not valid after this date.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="b4794-121">Nombre del firmante</span><span class="sxs-lookup"><span data-stu-id="b4794-121">Subject Name</span></span>                                | <span data-ttu-id="b4794-122">Nombre de la persona o entidad para la que se emite el certificado.</span><span class="sxs-lookup"><span data-stu-id="b4794-122">Name of the person or entity to whom the certificate is being issued.</span></span> <span data-ttu-id="b4794-123">Este campo también puede incluir la organización, la unidad organizativa, la localidad, el estado o la provincia del destinatario del certificado, y el país o la región.</span><span class="sxs-lookup"><span data-stu-id="b4794-123">This field can also include the certificate recipient's organization, organization unit, locality, state or province, and country/region.</span></span> |
| <span data-ttu-id="b4794-124">Algoritmo y parámetros de clave pública de sujeto</span><span class="sxs-lookup"><span data-stu-id="b4794-124">Subject Public Key Algorithm and Parameters</span></span> | <span data-ttu-id="b4794-125">El algoritmo y los parámetros utilizados para la [*clave pública*](../secgloss/p-gly.md)del sujeto.</span><span class="sxs-lookup"><span data-stu-id="b4794-125">The algorithm and any parameters used for the subject's [*public key*](../secgloss/p-gly.md).</span></span>                                                                       |
| <span data-ttu-id="b4794-126">Clave pública de asunto</span><span class="sxs-lookup"><span data-stu-id="b4794-126">Subject Public Key</span></span>                          | <span data-ttu-id="b4794-127">La clave pública real (una cadena de bits).</span><span class="sxs-lookup"><span data-stu-id="b4794-127">The actual public key (a bit string).</span></span>                                                                                                                                                                           |
| <span data-ttu-id="b4794-128">Firma</span><span class="sxs-lookup"><span data-stu-id="b4794-128">Signature</span></span>                                   | <span data-ttu-id="b4794-129">Firma proporcionada por el emisor.</span><span class="sxs-lookup"><span data-stu-id="b4794-129">Signature as provided by the issuer.</span></span>                                                                                                                                                                            |



 

<span data-ttu-id="b4794-130">Un certificado puede contener los elementos siguientes, en función de la versión [*X. 509*](../secgloss/x-gly.md) del certificado.</span><span class="sxs-lookup"><span data-stu-id="b4794-130">A certificate can contain the following items, depending on the [*X.509*](../secgloss/x-gly.md) version of the certificate.</span></span>



| <span data-ttu-id="b4794-131">Campo opcional</span><span class="sxs-lookup"><span data-stu-id="b4794-131">Optional field</span></span>    | <span data-ttu-id="b4794-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4794-132">Description</span></span>                                                                                                                                                                                               |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4794-133">IDENTIFICADOR único del emisor</span><span class="sxs-lookup"><span data-stu-id="b4794-133">Issuer Unique ID</span></span>  | <span data-ttu-id="b4794-134">Se usa para hacer que el nombre del emisor no sea ambiguo si lo ha usado más de una entidad.</span><span class="sxs-lookup"><span data-stu-id="b4794-134">Used to make the issuer name unambiguous if it has been used by more than one entity.</span></span> <span data-ttu-id="b4794-135">Presente solo en las versiones [*X. 509*](../secgloss/x-gly.md) 2,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b4794-135">Present only in versions [*X.509*](../secgloss/x-gly.md) 2.0 or later.</span></span><br/> |
| <span data-ttu-id="b4794-136">IDENTIFICADOR único del firmante</span><span class="sxs-lookup"><span data-stu-id="b4794-136">Subject unique ID</span></span> | <span data-ttu-id="b4794-137">Se usa para hacer que el nombre del firmante no sea ambiguo si lo ha utilizado más de una entidad.</span><span class="sxs-lookup"><span data-stu-id="b4794-137">Used to make the subject name unambiguous if it has been used by more than one entity.</span></span> <span data-ttu-id="b4794-138">Presente solo en X. 509 2,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b4794-138">Present only in X.509 2.0 or later.</span></span><br/>                                                                     |
| <span data-ttu-id="b4794-139">Extensiones</span><span class="sxs-lookup"><span data-stu-id="b4794-139">Extensions</span></span>        | <span data-ttu-id="b4794-140">Para especificar las propiedades personalizadas deseadas.</span><span class="sxs-lookup"><span data-stu-id="b4794-140">For specifying any desired custom properties.</span></span> <span data-ttu-id="b4794-141">Se puede incluir cualquier número de campos de extensión en el certificado.</span><span class="sxs-lookup"><span data-stu-id="b4794-141">Any number of extension fields can be included in the certificate.</span></span> <span data-ttu-id="b4794-142">Presente solo en la versión X. 509 3,0.</span><span class="sxs-lookup"><span data-stu-id="b4794-142">Present only in version X.509 3.0.</span></span><br/>                                            |



 

> [!Note]  
> <span data-ttu-id="b4794-143">Los servicios de Certificate Server de Microsoft emiten certificados X. 509 versión 3.</span><span class="sxs-lookup"><span data-stu-id="b4794-143">Microsoft Certificate Services issues X.509 version 3 certificates.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b4794-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b4794-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4794-145">Propiedades de nombre</span><span class="sxs-lookup"><span data-stu-id="b4794-145">Name Properties</span></span>](name-properties.md)
</dt> </dl>

 

 
