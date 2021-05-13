---
description: Navega a la página del asistente del lado cliente que sigue a la página que hospeda las páginas HTML del lado servidor o finaliza el asistente si no hay más páginas del lado cliente.
title: Método WebWizardHost.FinalNext (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalNext
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 0699eb16-d6ef-46e3-bd02-d35512536275
ms.openlocfilehash: fa59a70c04e7f78a315955aeabb9477c6f28c80d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841846"
---
# <a name="webwizardhostfinalnext-method"></a><span data-ttu-id="4ad55-103">Método WebWizardHost.FinalNext</span><span class="sxs-lookup"><span data-stu-id="4ad55-103">WebWizardHost.FinalNext method</span></span>

<span data-ttu-id="4ad55-104">Navega a la página del asistente del lado cliente que sigue a la página que hospeda las páginas HTML del lado servidor o finaliza el asistente si no hay más páginas del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="4ad55-104">Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ad55-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ad55-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a><span data-ttu-id="4ad55-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ad55-106">Parameters</span></span>

<span data-ttu-id="4ad55-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4ad55-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ad55-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ad55-108">Remarks</span></span>

<span data-ttu-id="4ad55-109">Cuando el asistente muestra la última página HTML del  lado  servidor y el usuario hace clic en los botones Siguiente o Finalizar, el servidor invoca **FinalNext** en el controlador de eventos de ese botón.</span><span class="sxs-lookup"><span data-stu-id="4ad55-109">When the wizard is displaying the last server-side HTML page and the user clicks the **Next** or **Finish** button, the server invokes **FinalNext** in that button's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ad55-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ad55-110">Requirements</span></span>



| <span data-ttu-id="4ad55-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ad55-111">Requirement</span></span> | <span data-ttu-id="4ad55-112">Value</span><span class="sxs-lookup"><span data-stu-id="4ad55-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ad55-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ad55-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4ad55-114">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4ad55-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4ad55-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ad55-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4ad55-116">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4ad55-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4ad55-117">Header</span><span class="sxs-lookup"><span data-stu-id="4ad55-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ad55-118"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="4ad55-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4ad55-119">Idl</span><span class="sxs-lookup"><span data-stu-id="4ad55-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4ad55-120"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="4ad55-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




