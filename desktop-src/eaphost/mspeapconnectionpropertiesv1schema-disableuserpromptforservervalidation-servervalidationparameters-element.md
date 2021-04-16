---
title: Elemento DisableUserPromptForServerValidation (PEAP)
description: Obtenga información sobre el elemento DisableUserPromptForServerValidation (ServerValidationParameters). Indica si se debe solicitar la validación del servidor al usuario. | Elemento DisableUserPromptForServerValidation (PEAP)
ms.assetid: ddb09888-731b-4c67-939e-9f0e6769408b
keywords:
- Elemento DisableUserPromptForServerValidation EAPHost
topic_type:
- apiref
api_name:
- DisableUserPromptForServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 168ce6e371495901f2ed93fb69b605a807bc363c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105649351"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-peap"></a><span data-ttu-id="26686-106">Elemento DisableUserPromptForServerValidation (ServerValidationParameters) (PEAP)</span><span class="sxs-lookup"><span data-stu-id="26686-106">DisableUserPromptForServerValidation (ServerValidationParameters) element (PEAP)</span></span>

<span data-ttu-id="26686-107">El elemento **DisableUserPromptForServerValidation (ServerValidationParameters)** indica si se debe pedir al usuario la validación del servidor.</span><span class="sxs-lookup"><span data-stu-id="26686-107">The **DisableUserPromptForServerValidation (ServerValidationParameters)** element indicates whether the user should be asked for server validation.</span></span>

<span data-ttu-id="26686-108">Si **DisableUserPromptForServerValidation** es true, EAP-TLS realiza la validación del servidor sin intervención del usuario; Si se produce un error en la validación, EAP-TLS produce un error en la autenticación.</span><span class="sxs-lookup"><span data-stu-id="26686-108">If **DisableUserPromptForServerValidation** is TRUE, then EAP-TLS performs the server validation without user input; if the validation fails, EAP-TLS fails the authentication.</span></span> <span data-ttu-id="26686-109">Si **DisableUserPromptForServerValidation** es false, se solicita al usuario un certificado o un nombre de servidor validados, o una entidad de certificación raíz (CA).</span><span class="sxs-lookup"><span data-stu-id="26686-109">If **DisableUserPromptForServerValidation** is FALSE, the user is prompted for a validated server certificate or name, or root certificate authority (CA).</span></span>

<span data-ttu-id="26686-110">El elemento **DisableUserPromptForServerValidation** es opcional.</span><span class="sxs-lookup"><span data-stu-id="26686-110">The **DisableUserPromptForServerValidation** element is optional.</span></span>

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

<span data-ttu-id="26686-111">El elemento **DisableUserPromptForServerValidation** se define mediante el tipo complejo de [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="26686-111">The **DisableUserPromptForServerValidation** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="26686-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26686-112">Requirements</span></span>



| <span data-ttu-id="26686-113">Role</span><span class="sxs-lookup"><span data-stu-id="26686-113">Role</span></span> | <span data-ttu-id="26686-114">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="26686-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="26686-115">Remoto</span><span class="sxs-lookup"><span data-stu-id="26686-115">Client</span></span><br/> | <span data-ttu-id="26686-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="26686-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="26686-117">Servidor</span><span class="sxs-lookup"><span data-stu-id="26686-117">Server</span></span><br/> | <span data-ttu-id="26686-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="26686-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26686-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="26686-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="26686-120">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="26686-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="26686-121">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="26686-121">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="26686-122">**Posibles elementos primarios inmediatos en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="26686-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="26686-123">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="26686-123">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="26686-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="26686-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="26686-125">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="26686-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="26686-126">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="26686-126">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="26686-127">Elementos de esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="26686-127">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





