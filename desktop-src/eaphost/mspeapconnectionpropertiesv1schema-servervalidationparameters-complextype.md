---
title: Tipo complejo de ServerValidationParameters (PEAP)
description: Obtenga información sobre el tipo complejo de ServerValidationParameters. Este tipo contiene información sobre cómo realizar la validación del servidor. | Tipo complejo de ServerValidationParameters (PEAP)
ms.assetid: 65b3199c-9462-447b-b560-0713348f9130
keywords:
- Tipo complejo ServerValidationParameters EAPHost
topic_type:
- apiref
api_name:
- ServerValidationParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42416723c4aaa86665f09ee8aa01d5dc1463c522
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003506"
---
# <a name="servervalidationparameters-complex-type-peap"></a><span data-ttu-id="7f771-106">Tipo complejo de ServerValidationParameters (PEAP)</span><span class="sxs-lookup"><span data-stu-id="7f771-106">ServerValidationParameters complex type (PEAP)</span></span>

<span data-ttu-id="7f771-107">El tipo complejo **ServerValidationParameters** contiene información sobre cómo realizar la validación del servidor.</span><span class="sxs-lookup"><span data-stu-id="7f771-107">The **ServerValidationParameters** complex type contains information about how to perform server validation.</span></span>

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="complextype"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="PerformServerValidation"
        type="boolean"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7f771-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7f771-108">Child elements</span></span>



| <span data-ttu-id="7f771-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="7f771-109">Element</span></span>                                                                                                                                                    | <span data-ttu-id="7f771-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="7f771-110">Type</span></span>        | <span data-ttu-id="7f771-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7f771-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f771-112">**DisableUserPromptForServerValidation**</span><span class="sxs-lookup"><span data-stu-id="7f771-112">**DisableUserPromptForServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | <span data-ttu-id="7f771-113">boolean</span><span class="sxs-lookup"><span data-stu-id="7f771-113">boolean</span></span>     | <span data-ttu-id="7f771-114">Indica si se debe solicitar al usuario la validación del servidor.</span><span class="sxs-lookup"><span data-stu-id="7f771-114">Indicates whether the user should be asked for server validation.</span></span> <br/> <span data-ttu-id="7f771-115">Si [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) es true, PEAP realiza la validación del servidor sin intervención del usuario; Si se produce un error en la validación, PEAP produce un error en la autenticación.</span><span class="sxs-lookup"><span data-stu-id="7f771-115">If [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is TRUE, then PEAP performs the server validation without user input; if the validation fails, PEAP fails the authentication.</span></span><br/> <span data-ttu-id="7f771-116">Si [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) es false, se solicita al usuario un certificado o un nombre de servidor validados, o una entidad de certificación raíz (CA).</span><span class="sxs-lookup"><span data-stu-id="7f771-116">If [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is FALSE, the user is prompted for a validated server certificate or name, or root certification authority (CA).</span></span><br/> <span data-ttu-id="7f771-117">El elemento [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="7f771-117">The [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="7f771-118">**ServerNames**</span><span class="sxs-lookup"><span data-stu-id="7f771-118">**ServerNames**</span></span>](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | <span data-ttu-id="7f771-119">complexType</span><span class="sxs-lookup"><span data-stu-id="7f771-119">complextype</span></span> | <span data-ttu-id="7f771-120">Representa una lista de servidores en los que el cliente confía.</span><span class="sxs-lookup"><span data-stu-id="7f771-120">Represents a list of servers the client trusts.</span></span> <span data-ttu-id="7f771-121">Cada nombre de servidor está delimitado por punto y coma, y se puede representar mediante expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="7f771-121">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <br/> <span data-ttu-id="7f771-122">El elemento [**servernames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="7f771-122">The [**ServerNames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="7f771-123">**TrustedRootCA**</span><span class="sxs-lookup"><span data-stu-id="7f771-123">**TrustedRootCA**</span></span>](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | <span data-ttu-id="7f771-124">hexBinary</span><span class="sxs-lookup"><span data-stu-id="7f771-124">hexBinary</span></span>   | <span data-ttu-id="7f771-125">Captura la impresión en miniatura de las entidades de certificación (CA) raíz en las que confía el cliente.</span><span class="sxs-lookup"><span data-stu-id="7f771-125">Captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span> <br/> <span data-ttu-id="7f771-126">La impresión en miniatura es una cadena hexadecimal que contiene el hash SHA-1 del certificado.</span><span class="sxs-lookup"><span data-stu-id="7f771-126">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate</span></span><br/> <span data-ttu-id="7f771-127">El elemento [**TrustedRootCA**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="7f771-127">The [**TrustedRootCA**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="attributes"></a><span data-ttu-id="7f771-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="7f771-128">Attributes</span></span>



| <span data-ttu-id="7f771-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="7f771-129">Name</span></span>                    | <span data-ttu-id="7f771-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="7f771-130">Type</span></span>    | <span data-ttu-id="7f771-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="7f771-131">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f771-132">PerformServerValidation</span><span class="sxs-lookup"><span data-stu-id="7f771-132">PerformServerValidation</span></span> | <span data-ttu-id="7f771-133">boolean</span><span class="sxs-lookup"><span data-stu-id="7f771-133">boolean</span></span> | <span data-ttu-id="7f771-134">Windows 7 o posterior: indica si se realiza la validación del servidor.</span><span class="sxs-lookup"><span data-stu-id="7f771-134">Windows 7 or later: Indicates whether server validation is performed.</span></span> <span data-ttu-id="7f771-135">El elemento [**PerformServerValidation**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="7f771-135">The [**PerformServerValidation**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md) element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7f771-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f771-136">Requirements</span></span>



| <span data-ttu-id="7f771-137">Role</span><span class="sxs-lookup"><span data-stu-id="7f771-137">Role</span></span> | <span data-ttu-id="7f771-138">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="7f771-138">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="7f771-139">Remoto</span><span class="sxs-lookup"><span data-stu-id="7f771-139">Client</span></span><br/> | <span data-ttu-id="7f771-140">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7f771-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7f771-141">Servidor</span><span class="sxs-lookup"><span data-stu-id="7f771-141">Server</span></span><br/> | <span data-ttu-id="7f771-142">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7f771-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7f771-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f771-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f771-144">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="7f771-144">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="7f771-145">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="7f771-145">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="7f771-146">Tipos complejos de esquema de mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="7f771-146">mspeapconnectionpropertiesv1 Schema Complex Types</span></span>](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="7f771-147">**AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="7f771-147">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





