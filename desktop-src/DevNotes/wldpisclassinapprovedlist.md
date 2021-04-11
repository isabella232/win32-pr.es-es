---
description: Llama a la biblioteca para validar si se puede llamar a un CLSID determinado.
ms.assetid: 94C8731B-88FD-4240-BF5D-2CD67C41B063
title: Función WldpIsClassInApprovedList (WLDP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsClassInApprovedList
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 01762c60a3f1aef1574cc218ace9988669175efe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152781"
---
# <a name="wldpisclassinapprovedlist-function"></a><span data-ttu-id="146d9-103">WldpIsClassInApprovedList función)</span><span class="sxs-lookup"><span data-stu-id="146d9-103">WldpIsClassInApprovedList function</span></span>

<span data-ttu-id="146d9-104">Llama a la biblioteca para validar si se puede llamar a un **CLSID** determinado.</span><span class="sxs-lookup"><span data-stu-id="146d9-104">Calls the library to validate if a particular **CLSID** is safe to be called.</span></span> <span data-ttu-id="146d9-105">La función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="146d9-105">The function has no associated import library.</span></span> <span data-ttu-id="146d9-106">Debe utilizar las funciones LoadLibrary y GetProcAddress para vincular dinámicamente a wldp.dll.</span><span class="sxs-lookup"><span data-stu-id="146d9-106">You must use the LoadLibrary and GetProcAddress functions to dynamically link to wldp.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="146d9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="146d9-107">Syntax</span></span>


```C++
HRESULT WINAPI WldpIsClassInApprovedList(
        REFCLSID               classID,
  _In_  PWLDP_HOST_INFORMATION hostInformation,
  _Out_ PBOOL                  isApproved,
        DWORD                  optionalFlags
);
```



## <a name="parameters"></a><span data-ttu-id="146d9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="146d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="146d9-109">*classID*</span><span class="sxs-lookup"><span data-stu-id="146d9-109">*classID*</span></span> 
</dt> <dd>

<span data-ttu-id="146d9-110">IDENTIFICADOR de clase COM cuya aprobación se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="146d9-110">The COM class ID to check for approval.</span></span>

</dd> <dt>

<span data-ttu-id="146d9-111">*hostInformation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="146d9-111">*hostInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="146d9-112">Una estructura de [**\_ \_ información del host de WLDP**](wldp-host-information.md) que identifica el host que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="146d9-112">A [**WLDP\_HOST\_INFORMATION**](wldp-host-information.md) structure identifying the host to be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="146d9-113">*isApproved* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="146d9-113">*isApproved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="146d9-114">Si se completa correctamente, contiene **true** si se aprueba el identificador de clase; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="146d9-114">On successful completion, contains **TRUE** if the class ID is approved; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="146d9-115">*optionalFlags*</span><span class="sxs-lookup"><span data-stu-id="146d9-115">*optionalFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="146d9-116">Este parámetro está reservado y debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="146d9-116">This parameter is reserved and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="146d9-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="146d9-117">Return value</span></span>

<span data-ttu-id="146d9-118">Este método devuelve **S \_ correcto** si es correcto o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="146d9-118">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="146d9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="146d9-119">Requirements</span></span>



| <span data-ttu-id="146d9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="146d9-120">Requirement</span></span> | <span data-ttu-id="146d9-121">Value</span><span class="sxs-lookup"><span data-stu-id="146d9-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="146d9-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="146d9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="146d9-123">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="146d9-123">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="146d9-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="146d9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="146d9-125">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="146d9-125">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="146d9-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="146d9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="146d9-127"><dt>WLDP. h</dt></span><span class="sxs-lookup"><span data-stu-id="146d9-127"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="146d9-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="146d9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="146d9-129"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="146d9-129"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




