---
description: Compara dos tokens de acceso y determina si son equivalentes con respecto a una llamada a la función AccessCheck.
ms.assetid: 3a07ddc6-9748-4f96-a597-2af6b4282e56
title: Función NtCompareTokens (Ntseapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtCompareTokens
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: d4d0f35bff8fa65e0e09be32a55281b5118f244c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652563"
---
# <a name="ntcomparetokens-function"></a><span data-ttu-id="fee85-103">NtCompareTokens función)</span><span class="sxs-lookup"><span data-stu-id="fee85-103">NtCompareTokens function</span></span>

<span data-ttu-id="fee85-104">La función **NtCompareTokens** compara dos [*tokens de acceso*](/windows/desktop/SecGloss/a-gly) y determina si son equivalentes con respecto a una llamada a la función [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) .</span><span class="sxs-lookup"><span data-stu-id="fee85-104">The **NtCompareTokens** function compares two [*access tokens*](/windows/desktop/SecGloss/a-gly) and determines whether they are equivalent with respect to a call to the [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="fee85-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fee85-105">Syntax</span></span>


```C++
NTSTATUS NTAPI NtCompareTokens(
  _In_  HANDLE   FirstTokenHandle,
  _In_  HANDLE   SecondTokenHandle,
  _Out_ PBOOLEAN Equal
);
```



## <a name="parameters"></a><span data-ttu-id="fee85-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fee85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fee85-107">*FirstTokenHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fee85-107">*FirstTokenHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fee85-108">Identificador del primer token de acceso que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="fee85-108">A handle to the first access token to compare.</span></span> <span data-ttu-id="fee85-109">El token debe estar abierto para el acceso a la **\_ consulta de tokens** .</span><span class="sxs-lookup"><span data-stu-id="fee85-109">The token must be open for **TOKEN\_QUERY** access.</span></span>

</dd> <dt>

<span data-ttu-id="fee85-110">*SecondTokenHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fee85-110">*SecondTokenHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fee85-111">Identificador del segundo token de acceso que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="fee85-111">A handle to the second access token to compare.</span></span> <span data-ttu-id="fee85-112">El token debe estar abierto para el acceso a la **\_ consulta de tokens** .</span><span class="sxs-lookup"><span data-stu-id="fee85-112">The token must be open for **TOKEN\_QUERY** access.</span></span>

</dd> <dt>

<span data-ttu-id="fee85-113">*Igual* \[ a enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fee85-113">*Equal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fee85-114">Un puntero a una variable que recibe un valor que indica si los tokens representados por los parámetros *FirstTokenHandle* y *SecondTokenHandle* son equivalentes.</span><span class="sxs-lookup"><span data-stu-id="fee85-114">A pointer to a variable that receives a value that indicates whether the tokens represented by the *FirstTokenHandle* and *SecondTokenHandle* parameters are equivalent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fee85-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fee85-115">Return value</span></span>

<span data-ttu-id="fee85-116">Si la función se ejecuta correctamente, la función devuelve el estado \_ Success.</span><span class="sxs-lookup"><span data-stu-id="fee85-116">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="fee85-117">Si se produce un error en la función, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="fee85-117">If the function fails, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fee85-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fee85-118">Remarks</span></span>

<span data-ttu-id="fee85-119">Dos tokens de control de acceso se consideran equivalentes si se cumplen todas las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="fee85-119">Two access control tokens are considered to be equivalent if all of the following conditions are true:</span></span>

-   <span data-ttu-id="fee85-120">Cada [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) que se encuentra en cualquiera de los tokens también está presente en el otro token.</span><span class="sxs-lookup"><span data-stu-id="fee85-120">Every [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) that is present in either token is also present in the other token.</span></span>
-   <span data-ttu-id="fee85-121">Ninguno de los tokens o ambos están restringidos.</span><span class="sxs-lookup"><span data-stu-id="fee85-121">Neither or both of the tokens are restricted.</span></span>
-   <span data-ttu-id="fee85-122">Si ambos tokens están restringidos, todos los SID que están restringidos en un token también están restringidos en el otro token.</span><span class="sxs-lookup"><span data-stu-id="fee85-122">If both tokens are restricted, every SID that is restricted in one token is also restricted in the other token.</span></span>
-   <span data-ttu-id="fee85-123">Cada privilegio presente en cualquiera de los tokens también está presente en el otro token.</span><span class="sxs-lookup"><span data-stu-id="fee85-123">Every privilege present in either token is also present in the other token.</span></span>

<span data-ttu-id="fee85-124">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="fee85-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="fee85-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fee85-125">Requirements</span></span>



| <span data-ttu-id="fee85-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fee85-126">Requirement</span></span> | <span data-ttu-id="fee85-127">Value</span><span class="sxs-lookup"><span data-stu-id="fee85-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fee85-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fee85-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fee85-129">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fee85-129">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fee85-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fee85-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fee85-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fee85-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fee85-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fee85-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fee85-133"><dt>Ntseapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fee85-133"><dt>Ntseapi.h</dt></span></span> </dl> |
| <span data-ttu-id="fee85-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fee85-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fee85-135"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fee85-135"><dt>Ntdll.dll</dt></span></span> </dl> |



 

