---
description: La función AuthzFreeCentralAccessPolicyCallback es una función definida por la aplicación que libera la memoria asignada por la función AuthzGetCentralAccessPolicyCallback.
ms.assetid: F0859A67-4D20-4189-8F35-A78034E41E6A
title: Función de devolución de llamada AuthzFreeCentralAccessPolicyCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: d2139c9fa106b6070a3c043d417bdbf23379084b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279640"
---
# <a name="authzfreecentralaccesspolicycallback-callback-function"></a><span data-ttu-id="66dd3-103">Función de devolución de llamada AuthzFreeCentralAccessPolicyCallback</span><span class="sxs-lookup"><span data-stu-id="66dd3-103">AuthzFreeCentralAccessPolicyCallback callback function</span></span>

<span data-ttu-id="66dd3-104">La función *AuthzFreeCentralAccessPolicyCallback* es una función definida por la aplicación que libera la memoria asignada por la función [*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md) .</span><span class="sxs-lookup"><span data-stu-id="66dd3-104">The *AuthzFreeCentralAccessPolicyCallback* function is an application-defined function that frees memory allocated by the [*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md) function.</span></span> <span data-ttu-id="66dd3-105">*AuthzFreeCentralAccessPolicyCallback* es un marcador de posición para el nombre de la función definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="66dd3-105">*AuthzFreeCentralAccessPolicyCallback* is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="66dd3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66dd3-106">Syntax</span></span>


```C++
BOOL CALLBACK AuthzFreeCentralAccessPolicyCallback(
  _In_ PVOID pCentralAccessPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="66dd3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66dd3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66dd3-108">*pCentralAccessPolicy* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="66dd3-108">*pCentralAccessPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66dd3-109">Puntero a la Directiva de acceso central que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="66dd3-109">Pointer to the central access policy to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66dd3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66dd3-110">Return value</span></span>

<span data-ttu-id="66dd3-111">Si la función se ejecuta correctamente, la función devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="66dd3-111">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="66dd3-112">Si la función no puede realizar la evaluación, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="66dd3-112">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="66dd3-113">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para devolver un error a la función de comprobación de acceso.</span><span class="sxs-lookup"><span data-stu-id="66dd3-113">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="see-also"></a><span data-ttu-id="66dd3-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="66dd3-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66dd3-115">**AUTHZ \_ init \_ info**</span><span class="sxs-lookup"><span data-stu-id="66dd3-115">**AUTHZ\_INIT\_INFO**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[<span data-ttu-id="66dd3-116">*AuthzGetCentralAccessPolicyCallback*</span><span class="sxs-lookup"><span data-stu-id="66dd3-116">*AuthzGetCentralAccessPolicyCallback*</span></span>](authzgetcentralaccesspolicycallback-.md)
</dt> </dl>

 

 
