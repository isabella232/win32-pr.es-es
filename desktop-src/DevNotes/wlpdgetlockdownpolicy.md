---
description: Llama a la biblioteca para obtener el estado de seguridad relativo al host, y el script o MSI que se va a usar.
ms.assetid: 4CCDA3B7-7661-47F6-A015-720BDEAEDBB1
title: Función WldpGetLockdownPolicy (WLDP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpGetLockdownPolicy
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a8f5e4da11e8ce7443d9a9bab323742cfc1b3a9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538751"
---
# <a name="wldpgetlockdownpolicy-function"></a><span data-ttu-id="b7feb-103">WldpGetLockdownPolicy función)</span><span class="sxs-lookup"><span data-stu-id="b7feb-103">WldpGetLockdownPolicy function</span></span>

<span data-ttu-id="b7feb-104">Llama a la biblioteca para obtener el estado de seguridad relativo al host, y el script o MSI que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="b7feb-104">Calls the library to get the security state relative to the host, and script or msi to be used.</span></span> <span data-ttu-id="b7feb-105">La función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="b7feb-105">The function has no associated import library.</span></span> <span data-ttu-id="b7feb-106">Debe utilizar las funciones LoadLibrary y GetProcAddress para vincular dinámicamente a wldp.dll.</span><span class="sxs-lookup"><span data-stu-id="b7feb-106">You must use the LoadLibrary and GetProcAddress functions to dynamically link to wldp.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7feb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7feb-107">Syntax</span></span>


```C++
HRESULT WINAPI WldpGetLockdownPolicy(
  _In_opt_ PWLDP_HOST_INFORMATION hostInformation,
  _Out_    PDWORD                 lockdownState,
  _In_     DWORD                  lockdownFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b7feb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7feb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7feb-109">*hostInformation* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b7feb-109">*hostInformation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7feb-110">Estructura [**de \_ \_ información de host de WLDP**](wldp-host-information.md) que identifica el host y el archivo de origen que se van a evaluar.</span><span class="sxs-lookup"><span data-stu-id="b7feb-110">A [**WLDP\_HOST\_INFORMATION**](wldp-host-information.md) structure identifying the host and source file to be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="b7feb-111">*lockdownState* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b7feb-111">*lockdownState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7feb-112">Proporciona el valor seguro de la Directiva resultante.</span><span class="sxs-lookup"><span data-stu-id="b7feb-112">Provides the resulting policy secure value.</span></span> <span data-ttu-id="b7feb-113">Cuando! WLDP_LOCKDOWN_IS_OFF, UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b7feb-113">If !WLDP_LOCKDOWN_IS_OFF, then UMCI is enabled.</span></span> <span data-ttu-id="b7feb-114">También puede comprobar WLDP_LOCKDOWN_IS_AUDIT y WLDP_LOCKDOWN_IS_ENFORCE para determinar si una directiva está en modo de auditoría o de aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7feb-114">You can also check WLDP_LOCKDOWN_IS_AUDIT and WLDP_LOCKDOWN_IS_ENFORCE to determine if a policy is in audit or enforce mode.</span></span>
</dd> <dt>

<span data-ttu-id="b7feb-115">*lockdownFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7feb-115">*lockdownFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7feb-116">Se definen los siguientes valores de marca \_ WLDP \_ SKIPSIGNATUREVALIDATION 0x00000100: cuando se establece, se omite la validación de SaferIdentifyLevel, que omitirá si un script está firmado.</span><span class="sxs-lookup"><span data-stu-id="b7feb-116">The following flag values are defined WLDP\_FLAGS\_SKIPSIGNATUREVALIDATION 0x00000100 – when set, skip the SaferIdentifyLevel validation, which will ignore whether a script is signed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7feb-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7feb-117">Return value</span></span>

<span data-ttu-id="b7feb-118">Este método devuelve S \_ correcto si es correcto o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b7feb-118">This method returns S\_OK if successful or a failure code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7feb-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7feb-119">Remarks</span></span>

<span data-ttu-id="b7feb-120">Cuando se llama con \_ la información de host de WLDP \_ . SZSOURCE = null, se devuelve la Directiva genérica para el host.</span><span class="sxs-lookup"><span data-stu-id="b7feb-120">When called with WLDP\_HOST\_INFORMATION.szSource = NULL, the generic policy for the host is returned.</span></span>

<span data-ttu-id="b7feb-121">Cuando se llama con la información de host de WLDP \_ \_ . DWHOSTID = WLDP ID. de \_ host \_ \_ global, WLDP \_ información de host \_ . szSource debe ser NULL y la función devolverá la directiva global del sistema.</span><span class="sxs-lookup"><span data-stu-id="b7feb-121">When called with WLDP\_HOST\_INFORMATION.dwHostId = WLDP\_HOST\_ID\_GLOBAL, WLDP\_HOST\_INFORMATION.szSource must be NULL, and the function will return the global system policy.</span></span>

<span data-ttu-id="b7feb-122">DwFlag WLDP \_ Flags \_ SKIPSIGNATUREVALIDATION se puede usar para omitir la validación SaferIdentifyLevel (), que omitirá si un script está firmado.</span><span class="sxs-lookup"><span data-stu-id="b7feb-122">The dwFlag WLDP\_FLAGS\_SKIPSIGNATUREVALIDATION can be used to skip the SaferIdentifyLevel() validation, which will ignore whether a script is signed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7feb-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7feb-123">Requirements</span></span>



| <span data-ttu-id="b7feb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7feb-124">Requirement</span></span> | <span data-ttu-id="b7feb-125">Value</span><span class="sxs-lookup"><span data-stu-id="b7feb-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b7feb-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7feb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b7feb-127">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="b7feb-127">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b7feb-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7feb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b7feb-129">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="b7feb-129">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b7feb-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7feb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7feb-131"><dt>WLDP. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7feb-131"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7feb-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b7feb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7feb-133"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7feb-133"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




