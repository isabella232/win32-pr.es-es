---
description: La función AuthzGetCentralAccessPolicyCallback es una función definida por la aplicación que recupera la Directiva de acceso central. AuthzGetCentralAccessPolicyCallback es un marcador de posición para el nombre de la función definida por la aplicación.
ms.assetid: 1D5831EF-ACA8-4EE9-A7C1-E1A3CB74CEC0
title: Función de devolución de llamada AuthzGetCentralAccessPolicyCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzGetCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b96832fa647fde920a70ac3d6608c8ebb0048892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653098"
---
# <a name="authzgetcentralaccesspolicycallback-callback-function"></a><span data-ttu-id="48b69-104">Función de devolución de llamada AuthzGetCentralAccessPolicyCallback</span><span class="sxs-lookup"><span data-stu-id="48b69-104">AuthzGetCentralAccessPolicyCallback callback function</span></span>

<span data-ttu-id="48b69-105">La función *AuthzGetCentralAccessPolicyCallback* es una función definida por la aplicación que recupera la Directiva de acceso central.</span><span class="sxs-lookup"><span data-stu-id="48b69-105">The *AuthzGetCentralAccessPolicyCallback* function is an application-defined function that retrieves the central access policy.</span></span> <span data-ttu-id="48b69-106">*AuthzGetCentralAccessPolicyCallback* es un marcador de posición para el nombre de la función definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="48b69-106">*AuthzGetCentralAccessPolicyCallback* is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="48b69-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48b69-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzGetCentralAccessPolicyCallback (
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PSID                        capid,
  _In_opt_ PVOID                       pArgs,
  _Out_    PBOOL                       pCentralAccessPolicyApplicable,
  _Out_    PVOID                       ppCentralAccessPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="48b69-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48b69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48b69-109">*hAuthzClientContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48b69-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48b69-110">Identificador del contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="48b69-110">Handle to the client context.</span></span>

</dd> <dt>

<span data-ttu-id="48b69-111">*capid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48b69-111">*capid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48b69-112">IDENTIFICADOR de la Directiva de acceso central que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="48b69-112">ID of the central access policy to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="48b69-113">*pArgs* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="48b69-113">*pArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="48b69-114">Argumentos opcionales que se pasaron a la función [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) a través del miembro **OptionalArguments** de la estructura de [**\_ \_ solicitud de acceso de AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_access_request) .</span><span class="sxs-lookup"><span data-stu-id="48b69-114">Optional arguments that were passed to the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function through the **OptionalArguments** member of the [**AUTHZ\_ACCESS\_REQUEST**](/windows/desktop/api/Authz/ns-authz-authz_access_request) structure.</span></span>

</dd> <dt>

<span data-ttu-id="48b69-115">*pCentralAccessPolicyApplicable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="48b69-115">*pCentralAccessPolicyApplicable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48b69-116">Puntero a un valor booleano que el administrador de recursos utiliza para indicar si se debe usar una directiva de acceso central durante la evaluación del acceso.</span><span class="sxs-lookup"><span data-stu-id="48b69-116">Pointer to a Boolean value that the resource manager uses to indicate whether a central access policy should be used during access evaluation.</span></span>

</dd> <dt>

<span data-ttu-id="48b69-117">*ppCentralAccessPolicy* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="48b69-117">*ppCentralAccessPolicy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48b69-118">Puntero a la Directiva de acceso central (CAP) que se va a usar para evaluar el acceso.</span><span class="sxs-lookup"><span data-stu-id="48b69-118">Pointer to the central access policy (CAP) to be used for evaluating access.</span></span> <span data-ttu-id="48b69-119">Si este valor es **null**, se aplica el límite predeterminado.</span><span class="sxs-lookup"><span data-stu-id="48b69-119">If this value is **NULL**, the default CAP is applied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48b69-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48b69-120">Return value</span></span>

<span data-ttu-id="48b69-121">Si la función se ejecuta correctamente, la función devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="48b69-121">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="48b69-122">Si la función no puede realizar la evaluación, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="48b69-122">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="48b69-123">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para devolver un error a la función de comprobación de acceso.</span><span class="sxs-lookup"><span data-stu-id="48b69-123">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="requirements"></a><span data-ttu-id="48b69-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48b69-124">Requirements</span></span>



| <span data-ttu-id="48b69-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="48b69-125">Requirement</span></span> | <span data-ttu-id="48b69-126">Value</span><span class="sxs-lookup"><span data-stu-id="48b69-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="48b69-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48b69-127">Minimum supported client</span></span><br/> | <span data-ttu-id="48b69-128">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="48b69-128">Windows 8 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="48b69-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48b69-129">Minimum supported server</span></span><br/> | <span data-ttu-id="48b69-130">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="48b69-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="48b69-131">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="48b69-131">Redistributable</span></span><br/>          | <span data-ttu-id="48b69-132">Paquete de herramientas de administración de Windows Server 2003 en Windows XP</span><span class="sxs-lookup"><span data-stu-id="48b69-132">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48b69-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="48b69-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48b69-134">**\_solicitud de acceso de AUTHZ \_**</span><span class="sxs-lookup"><span data-stu-id="48b69-134">**AUTHZ\_ACCESS\_REQUEST**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_access_request)
</dt> <dt>

[<span data-ttu-id="48b69-135">**AUTHZ \_ init \_ info**</span><span class="sxs-lookup"><span data-stu-id="48b69-135">**AUTHZ\_INIT\_INFO**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[<span data-ttu-id="48b69-136">**AuthzAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="48b69-136">**AuthzAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> </dl>

 

