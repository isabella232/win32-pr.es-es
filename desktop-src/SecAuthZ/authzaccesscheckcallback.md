---
description: Una función definida por la aplicación que controla las entradas de control de acceso (ACE) de devolución de llamada durante una comprobación de acceso.
ms.assetid: e8a510e6-0739-4765-ad07-3bcb1b9c905c
title: Función de devolución de llamada AuthzAccessCheckCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzAccessCheckCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 82e100092dd7c59e9cc689aa8723365fae8bed29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279642"
---
# <a name="authzaccesscheckcallback-callback-function"></a><span data-ttu-id="f993f-103">Función de devolución de llamada AuthzAccessCheckCallback</span><span class="sxs-lookup"><span data-stu-id="f993f-103">AuthzAccessCheckCallback callback function</span></span>

<span data-ttu-id="f993f-104">La función **AuthzAccessCheckCallback** es una función definida por la aplicación que controla [*las entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) de devolución de llamada durante una comprobación de acceso.</span><span class="sxs-lookup"><span data-stu-id="f993f-104">The **AuthzAccessCheckCallback** function is an application-defined function that handles callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) during an access check.</span></span> <span data-ttu-id="f993f-105">**AuthzAccessCheckCallback** es un marcador de posición para el nombre de la función definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f993f-105">**AuthzAccessCheckCallback** is a placeholder for the application-defined function name.</span></span> <span data-ttu-id="f993f-106">La aplicación registra esta devolución de llamada mediante una llamada a [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).</span><span class="sxs-lookup"><span data-stu-id="f993f-106">The application registers this callback by calling [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).</span></span>

## <a name="syntax"></a><span data-ttu-id="f993f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f993f-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzAccessCheckCallback(
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PACE_HEADER                 pAce,
  _In_opt_ PVOID                       pArgs,
  _Inout_  PBOOL                       pbAceApplicable
);
```



## <a name="parameters"></a><span data-ttu-id="f993f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f993f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f993f-109">*hAuthzClientContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f993f-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f993f-110">Identificador de un contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="f993f-110">A handle to a client context.</span></span>

</dd> <dt>

<span data-ttu-id="f993f-111">*pAce* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f993f-111">*pAce* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f993f-112">Puntero a la ACE que se va a evaluar para su inclusión en la llamada a la función [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="f993f-112">A pointer to the ACE to evaluate for inclusion in the call to the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span>

</dd> <dt>

<span data-ttu-id="f993f-113">*pArgs* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f993f-113">*pArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f993f-114">Datos pasados en el parámetro *DynamicGroupArgs* de la llamada a [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) o [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck).</span><span class="sxs-lookup"><span data-stu-id="f993f-114">Data passed in the *DynamicGroupArgs* parameter of the call to [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) or [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck).</span></span>

</dd> <dt>

<span data-ttu-id="f993f-115">*pbAceApplicable* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f993f-115">*pbAceApplicable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f993f-116">Puntero a una variable booleana que recibe los resultados de la evaluación de la lógica definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f993f-116">A pointer to a Boolean variable that receives the results of the evaluation of the logic defined by the application.</span></span>

<span data-ttu-id="f993f-117">Los resultados son **verdaderos** si la lógica determina que la ACE es aplicable y se incluirá en la llamada a [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck); de lo contrario, los resultados son **false**.</span><span class="sxs-lookup"><span data-stu-id="f993f-117">The results are **TRUE** if the logic determines that the ACE is applicable and will be included in the call to [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck); otherwise, the results are **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f993f-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f993f-118">Return value</span></span>

<span data-ttu-id="f993f-119">Si la función se ejecuta correctamente, la función devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="f993f-119">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="f993f-120">Si la función no puede realizar la evaluación, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="f993f-120">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="f993f-121">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para devolver un error a la función de comprobación de acceso.</span><span class="sxs-lookup"><span data-stu-id="f993f-121">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="remarks"></a><span data-ttu-id="f993f-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f993f-122">Remarks</span></span>

<span data-ttu-id="f993f-123">Las variables de atributo de seguridad deben estar presentes en el contexto del cliente si se hace referencia a en una expresión condicional; de lo contrario, el término de la expresión condicional que hace referencia a ellos se evaluará como desconocido.</span><span class="sxs-lookup"><span data-stu-id="f993f-123">Security attribute variables must be present in the client context if referred to in a conditional expression, otherwise the conditional expression term referencing them will evaluate to unknown.</span></span>

<span data-ttu-id="f993f-124">Para obtener más información, consulte la información general [sobre el funcionamiento de AccessCheck](how-dacls-control-access-to-an-object.md) y la Directiva de [autorización centralizada](centralized-authorization-policy.md) .</span><span class="sxs-lookup"><span data-stu-id="f993f-124">For more information, see the [How AccessCheck Works](how-dacls-control-access-to-an-object.md) and [Centralized Authorization Policy](centralized-authorization-policy.md) overviews.</span></span>

## <a name="requirements"></a><span data-ttu-id="f993f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f993f-125">Requirements</span></span>



| <span data-ttu-id="f993f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f993f-126">Requirement</span></span> | <span data-ttu-id="f993f-127">Value</span><span class="sxs-lookup"><span data-stu-id="f993f-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="f993f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f993f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f993f-129">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f993f-129">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f993f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f993f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f993f-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f993f-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="f993f-132">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f993f-132">Redistributable</span></span><br/>          | <span data-ttu-id="f993f-133">Paquete de herramientas de administración de Windows Server 2003 en Windows XP</span><span class="sxs-lookup"><span data-stu-id="f993f-133">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f993f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f993f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f993f-135">Funciones básicas de Access Control</span><span class="sxs-lookup"><span data-stu-id="f993f-135">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="f993f-136">Directiva de autorización centralizada</span><span class="sxs-lookup"><span data-stu-id="f993f-136">Centralized Authorization Policy</span></span>](centralized-authorization-policy.md)
</dt> <dt>

[<span data-ttu-id="f993f-137">Cómo funciona AccessCheck</span><span class="sxs-lookup"><span data-stu-id="f993f-137">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="f993f-138">**AuthzAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="f993f-138">**AuthzAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> <dt>

[<span data-ttu-id="f993f-139">**AuthzCachedAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="f993f-139">**AuthzCachedAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[<span data-ttu-id="f993f-140">**AuthzInitializeRemoteResourceManager**</span><span class="sxs-lookup"><span data-stu-id="f993f-140">**AuthzInitializeRemoteResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[<span data-ttu-id="f993f-141">**AuthzInitializeResourceManager**</span><span class="sxs-lookup"><span data-stu-id="f993f-141">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

