---
description: Navega a la página del lado cliente inmediatamente anterior a la página que hospeda las páginas HTML del lado servidor.
title: Método WebWizardHost.FinalBack (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalBack
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: a0616388-cf94-4433-ae52-24f02f1d15ac
ms.openlocfilehash: f131050bb5dd4cfc4b8533857c306f566f12ec2d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841876"
---
# <a name="webwizardhostfinalback-method"></a><span data-ttu-id="bc785-103">Método WebWizardHost.FinalBack</span><span class="sxs-lookup"><span data-stu-id="bc785-103">WebWizardHost.FinalBack method</span></span>

<span data-ttu-id="bc785-104">Navega a la página del lado cliente inmediatamente anterior a la página que hospeda las páginas HTML del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="bc785-104">Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc785-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc785-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a><span data-ttu-id="bc785-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc785-106">Parameters</span></span>

<span data-ttu-id="bc785-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bc785-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc785-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc785-108">Remarks</span></span>

<span data-ttu-id="bc785-109">Cuando el asistente muestra la primera página del  lado servidor y el usuario hace clic en el botón Atrás, el servidor invoca **FinalBack** cuando el controlador de eventos del cliente lo notifica.</span><span class="sxs-lookup"><span data-stu-id="bc785-109">When the wizard displays the first server-side page and the user clicks the **Back** button, the server invokes **FinalBack** when notified of that event by the client's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc785-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc785-110">Requirements</span></span>



| <span data-ttu-id="bc785-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc785-111">Requirement</span></span> | <span data-ttu-id="bc785-112">Value</span><span class="sxs-lookup"><span data-stu-id="bc785-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc785-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc785-113">Minimum supported client</span></span><br/> | <span data-ttu-id="bc785-114">Solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="bc785-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bc785-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc785-115">Minimum supported server</span></span><br/> | <span data-ttu-id="bc785-116">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc785-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bc785-117">Header</span><span class="sxs-lookup"><span data-stu-id="bc785-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc785-118"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="bc785-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc785-119">Idl</span><span class="sxs-lookup"><span data-stu-id="bc785-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bc785-120"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="bc785-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




