---
description: Navega a la página del asistente del lado cliente que sigue a la página que hospeda las páginas HTML del lado servidor o finaliza el asistente si no hay más páginas del lado cliente.
title: Método WebWizardHost. FinalNext (Shldisp. h)
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
ms.openlocfilehash: 5693de342b03a9ee4b7ed04cf24d8cfa9ee8b784
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277795"
---
# <a name="webwizardhostfinalnext-method"></a><span data-ttu-id="63211-103">WebWizardHost. FinalNext, método</span><span class="sxs-lookup"><span data-stu-id="63211-103">WebWizardHost.FinalNext method</span></span>

<span data-ttu-id="63211-104">Navega a la página del asistente del lado cliente que sigue a la página que hospeda las páginas HTML del lado servidor o finaliza el asistente si no hay más páginas del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="63211-104">Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="63211-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63211-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a><span data-ttu-id="63211-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63211-106">Parameters</span></span>

<span data-ttu-id="63211-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="63211-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="63211-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63211-108">Remarks</span></span>

<span data-ttu-id="63211-109">Cuando el asistente muestra la última página HTML del servidor y el usuario hace clic en el botón **siguiente** o **Finalizar** , el servidor invoca **FinalNext** en el controlador de eventos de ese botón.</span><span class="sxs-lookup"><span data-stu-id="63211-109">When the wizard is displaying the last server-side HTML page and the user clicks the **Next** or **Finish** button, the server invokes **FinalNext** in that button's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="63211-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63211-110">Requirements</span></span>



| <span data-ttu-id="63211-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="63211-111">Requirement</span></span> | <span data-ttu-id="63211-112">Value</span><span class="sxs-lookup"><span data-stu-id="63211-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63211-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63211-113">Minimum supported client</span></span><br/> | <span data-ttu-id="63211-114">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="63211-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="63211-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63211-115">Minimum supported server</span></span><br/> | <span data-ttu-id="63211-116">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="63211-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="63211-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63211-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="63211-118"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="63211-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="63211-119">IDL</span><span class="sxs-lookup"><span data-stu-id="63211-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="63211-120"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="63211-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




