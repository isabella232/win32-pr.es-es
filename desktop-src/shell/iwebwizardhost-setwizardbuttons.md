---
description: Actualiza los botones atrás, siguiente y finalizar en el marco del asistente del cliente.
title: Método WebWizardHost. SetWizardButtons (Shldisp. h)
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
ms.openlocfilehash: 18af31eac1042e84a41e5651c517279869f03697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985786"
---
# <a name="webwizardhostsetwizardbuttons-method"></a><span data-ttu-id="dea84-103">WebWizardHost. SetWizardButtons, método</span><span class="sxs-lookup"><span data-stu-id="dea84-103">WebWizardHost.SetWizardButtons method</span></span>

<span data-ttu-id="dea84-104">Actualiza los botones **atrás**, **siguiente** y **Finalizar** en el marco del asistente del cliente.</span><span class="sxs-lookup"><span data-stu-id="dea84-104">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="dea84-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dea84-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a><span data-ttu-id="dea84-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dea84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dea84-107">*vbEnableBack* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dea84-107">*vbEnableBack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea84-108">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dea84-108">Type: **Boolean**</span></span>

<span data-ttu-id="dea84-109">Habilita el botón **atrás** .</span><span class="sxs-lookup"><span data-stu-id="dea84-109">Enables the **Back** button.</span></span>

</dd> <dt>

<span data-ttu-id="dea84-110">*vbEnableNext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dea84-110">*vbEnableNext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea84-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dea84-111">Type: **Boolean**</span></span>

<span data-ttu-id="dea84-112">Habilita el botón **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="dea84-112">Enables the **Next** button.</span></span>

</dd> <dt>

<span data-ttu-id="dea84-113">*vbLastPage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dea84-113">*vbLastPage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea84-114">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dea84-114">Type: **Boolean**</span></span>

<span data-ttu-id="dea84-115">Habilita el botón **Finalizar** .</span><span class="sxs-lookup"><span data-stu-id="dea84-115">Enables the **Finish** button.</span></span> <span data-ttu-id="dea84-116">Indica que se trata de la última página del servidor.</span><span class="sxs-lookup"><span data-stu-id="dea84-116">States that this is the last server-side page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dea84-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dea84-117">Remarks</span></span>

<span data-ttu-id="dea84-118">Asegúrese de implementar las funciones de controlador en cada página del servidor para la función alback () y en la siguiente (), correspondientes a los botones del asistente **atrás** y **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="dea84-118">Be sure to implement handler functions in each server-side page for OnBack() and OnNext(), corresponding to the wizard buttons **Back** and **Next**.</span></span> <span data-ttu-id="dea84-119">Las funciones alback () y alnext () responden a **SetWizardButtons**.</span><span class="sxs-lookup"><span data-stu-id="dea84-119">The OnBack() and OnNext() functions respond to **SetWizardButtons**.</span></span> <span data-ttu-id="dea84-120">En el momento adecuado, la función Next () llama a **SetWizardButtons** con *vbLastPage* = **true**, que puede habilitar un botón **Finalizar** .</span><span class="sxs-lookup"><span data-stu-id="dea84-120">At the appropriate time, the OnNext() function calls **SetWizardButtons** with *vbLastPage*=**true**, which can enable a **Finish** button.</span></span> <span data-ttu-id="dea84-121">El siguiente () también llama a [**FinalNext**](iwebwizardhost-finalnext.md) cuando un usuario hace clic en el botón **Finalizar** .</span><span class="sxs-lookup"><span data-stu-id="dea84-121">OnNext() also calls [**FinalNext**](iwebwizardhost-finalnext.md) when a user clicks the **Finish** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="dea84-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dea84-122">Requirements</span></span>



| <span data-ttu-id="dea84-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="dea84-123">Requirement</span></span> | <span data-ttu-id="dea84-124">Value</span><span class="sxs-lookup"><span data-stu-id="dea84-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dea84-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dea84-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dea84-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="dea84-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="dea84-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dea84-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dea84-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dea84-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dea84-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dea84-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="dea84-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dea84-130"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dea84-131">IDL</span><span class="sxs-lookup"><span data-stu-id="dea84-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dea84-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dea84-132"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




