---
description: Actualiza los botones Atrás, Siguiente y Finalizar en el marco del asistente del cliente.
title: Método WebWizardHost.SetWizardButtons (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetWizardButtons
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 863aa667-454c-40cd-8091-9bb456047b6c
ms.openlocfilehash: a1b2a79c7ea323c36371e08d3519e71e4c537935
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842626"
---
# <a name="webwizardhostsetwizardbuttons-method"></a><span data-ttu-id="1667c-103">Método WebWizardHost.SetWizardButtons</span><span class="sxs-lookup"><span data-stu-id="1667c-103">WebWizardHost.SetWizardButtons method</span></span>

<span data-ttu-id="1667c-104">Actualiza los **botones** **Atrás,** Siguiente **y** Finalizar en el marco del asistente del cliente.</span><span class="sxs-lookup"><span data-stu-id="1667c-104">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="1667c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1667c-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a><span data-ttu-id="1667c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1667c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1667c-107">*vbEnableBack* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1667c-107">*vbEnableBack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1667c-108">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1667c-108">Type: **Boolean**</span></span>

<span data-ttu-id="1667c-109">Habilita el **botón** Atrás.</span><span class="sxs-lookup"><span data-stu-id="1667c-109">Enables the **Back** button.</span></span>

</dd> <dt>

<span data-ttu-id="1667c-110">*vbEnableNext* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1667c-110">*vbEnableNext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1667c-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1667c-111">Type: **Boolean**</span></span>

<span data-ttu-id="1667c-112">Habilita el botón **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="1667c-112">Enables the **Next** button.</span></span>

</dd> <dt>

<span data-ttu-id="1667c-113">*vbLastPage* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1667c-113">*vbLastPage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1667c-114">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1667c-114">Type: **Boolean**</span></span>

<span data-ttu-id="1667c-115">Habilita el **botón** Finalizar.</span><span class="sxs-lookup"><span data-stu-id="1667c-115">Enables the **Finish** button.</span></span> <span data-ttu-id="1667c-116">Indica que esta es la última página del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="1667c-116">States that this is the last server-side page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1667c-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1667c-117">Remarks</span></span>

<span data-ttu-id="1667c-118">Asegúrese de implementar funciones de controlador en cada página del lado servidor para OnBack() y OnNext(), correspondientes a los botones del asistente **Atrás** y **Siguiente.**</span><span class="sxs-lookup"><span data-stu-id="1667c-118">Be sure to implement handler functions in each server-side page for OnBack() and OnNext(), corresponding to the wizard buttons **Back** and **Next**.</span></span> <span data-ttu-id="1667c-119">Las funciones OnBack() y OnNext() responden a **SetWizardButtons**.</span><span class="sxs-lookup"><span data-stu-id="1667c-119">The OnBack() and OnNext() functions respond to **SetWizardButtons**.</span></span> <span data-ttu-id="1667c-120">En el momento adecuado, la función OnNext() llama a **SetWizardButtons** con *vbLastPage* true , que = puede habilitar un **botón Finalizar.**</span><span class="sxs-lookup"><span data-stu-id="1667c-120">At the appropriate time, the OnNext() function calls **SetWizardButtons** with *vbLastPage*=**true**, which can enable a **Finish** button.</span></span> <span data-ttu-id="1667c-121">OnNext() también llama a [**FinalNext**](iwebwizardhost-finalnext.md) cuando un usuario hace clic en **el botón** Finalizar.</span><span class="sxs-lookup"><span data-stu-id="1667c-121">OnNext() also calls [**FinalNext**](iwebwizardhost-finalnext.md) when a user clicks the **Finish** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="1667c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1667c-122">Requirements</span></span>



| <span data-ttu-id="1667c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1667c-123">Requirement</span></span> | <span data-ttu-id="1667c-124">Value</span><span class="sxs-lookup"><span data-stu-id="1667c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1667c-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1667c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1667c-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1667c-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1667c-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1667c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1667c-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1667c-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1667c-129">Header</span><span class="sxs-lookup"><span data-stu-id="1667c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1667c-130"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="1667c-130"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1667c-131">Idl</span><span class="sxs-lookup"><span data-stu-id="1667c-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1667c-132"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="1667c-132"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




