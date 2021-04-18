---
title: Tipo complejo de ServerValidationParameters (TLS)
description: Obtenga información sobre el tipo complejo de ServerValidationParameters. Este tipo contiene información sobre cómo realizar la validación del servidor. | Tipo complejo de ServerValidationParameters (TLS)
ms.assetid: 7a35c7f5-4cab-43d5-87dc-a4020811d3a9
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
ms.openlocfilehash: edebffd1f2023dd6f460505dc033e4505df338d7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698118"
---
# <a name="servervalidationparameters-complex-type-tls"></a><span data-ttu-id="430db-106">Tipo complejo de ServerValidationParameters (TLS)</span><span class="sxs-lookup"><span data-stu-id="430db-106">ServerValidationParameters Complex Type (TLS)</span></span>

<span data-ttu-id="430db-107">El tipo complejo **ServerValidationParameters** contiene información sobre cómo realizar la validación del servidor.</span><span class="sxs-lookup"><span data-stu-id="430db-107">The **ServerValidationParameters** complex type contains information about how to perform server validation.</span></span>

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="string"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="430db-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="430db-108">Child elements</span></span>



| <span data-ttu-id="430db-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="430db-109">Element</span></span>                                                                                                                                                    | <span data-ttu-id="430db-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="430db-110">Type</span></span>      | <span data-ttu-id="430db-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="430db-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="430db-112">**DisableUserPromptForServerValidation**</span><span class="sxs-lookup"><span data-stu-id="430db-112">**DisableUserPromptForServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | <span data-ttu-id="430db-113">boolean</span><span class="sxs-lookup"><span data-stu-id="430db-113">boolean</span></span>   | <span data-ttu-id="430db-114">Indica si se debe solicitar al usuario la validación del servidor.</span><span class="sxs-lookup"><span data-stu-id="430db-114">Indicates whether the user should be asked for server validation.</span></span> <br/> <span data-ttu-id="430db-115">Si [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) es true, EAP-TLS realiza la validación del servidor sin intervención del usuario; Si se produce un error en la validación, EAP-TLS produce un error en la autenticación.</span><span class="sxs-lookup"><span data-stu-id="430db-115">If [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is TRUE, then EAP-TLS performs the server validation without user input; if the validation fails, EAP-TLS fails the authentication.</span></span> <br/> <span data-ttu-id="430db-116">Si [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) es false, se solicita al usuario un certificado o un nombre de servidor validados, o una entidad de certificación raíz (CA).</span><span class="sxs-lookup"><span data-stu-id="430db-116">If [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is FALSE, the user is prompted for a validated server certificate or name, or root certificate authority (CA).</span></span><br/> <span data-ttu-id="430db-117">El elemento [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="430db-117">The [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="430db-118">**ServerNames**</span><span class="sxs-lookup"><span data-stu-id="430db-118">**ServerNames**</span></span>](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | <span data-ttu-id="430db-119">string</span><span class="sxs-lookup"><span data-stu-id="430db-119">string</span></span>    | <span data-ttu-id="430db-120">Representa una lista de servidores en los que el cliente confía.</span><span class="sxs-lookup"><span data-stu-id="430db-120">Represents a list of servers the client trusts.</span></span> <span data-ttu-id="430db-121">Cada nombre de servidor está delimitado por punto y coma, y se puede representar mediante expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="430db-121">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span><br/> <span data-ttu-id="430db-122">El elemento [**servernames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="430db-122">The [**ServerNames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="430db-123">**TrustedRootCA**</span><span class="sxs-lookup"><span data-stu-id="430db-123">**TrustedRootCA**</span></span>](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | <span data-ttu-id="430db-124">hexBinary</span><span class="sxs-lookup"><span data-stu-id="430db-124">hexBinary</span></span> | <span data-ttu-id="430db-125">Captura la impresión en miniatura de las entidades de certificación (CA) raíz en las que confía el cliente.</span><span class="sxs-lookup"><span data-stu-id="430db-125">Captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span> <br/> <span data-ttu-id="430db-126">La impresión en miniatura es una cadena hexadecimal que contiene el hash SHA-1 del certificado.</span><span class="sxs-lookup"><span data-stu-id="430db-126">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate</span></span><br/> <span data-ttu-id="430db-127">El elemento [**TrustedRootCA**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="430db-127">The [**TrustedRootCA**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="430db-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="430db-128">Requirements</span></span>



| <span data-ttu-id="430db-129">Role</span><span class="sxs-lookup"><span data-stu-id="430db-129">Role</span></span> | <span data-ttu-id="430db-130">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="430db-130">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="430db-131">Remoto</span><span class="sxs-lookup"><span data-stu-id="430db-131">Client</span></span><br/> | <span data-ttu-id="430db-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="430db-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="430db-133">Servidor</span><span class="sxs-lookup"><span data-stu-id="430db-133">Server</span></span><br/> | <span data-ttu-id="430db-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="430db-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="430db-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="430db-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="430db-136">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="430db-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="430db-137">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="430db-137">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="430db-138">Tipos complejos de esquema de eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="430db-138">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





