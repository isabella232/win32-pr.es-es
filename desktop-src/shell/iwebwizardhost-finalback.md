---
description: Navega a la página del lado cliente inmediatamente anterior a la página que hospeda las páginas HTML del lado servidor.
title: Método WebWizardHost. FinalBack (Shldisp. h)
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
ms.openlocfilehash: 704efbd4aae5a98ec01d8bd900e226144d25833d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910458"
---
# <a name="webwizardhostfinalback-method"></a><span data-ttu-id="51f96-103">WebWizardHost. FinalBack, método</span><span class="sxs-lookup"><span data-stu-id="51f96-103">WebWizardHost.FinalBack method</span></span>

<span data-ttu-id="51f96-104">Navega a la página del lado cliente inmediatamente anterior a la página que hospeda las páginas HTML del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="51f96-104">Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="51f96-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51f96-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a><span data-ttu-id="51f96-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51f96-106">Parameters</span></span>

<span data-ttu-id="51f96-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="51f96-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="51f96-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51f96-108">Remarks</span></span>

<span data-ttu-id="51f96-109">Cuando el asistente muestra la primera página del servidor y el usuario hace clic en el botón **atrás** , el servidor invoca **FinalBack** cuando el controlador de eventos del cliente notifica ese evento.</span><span class="sxs-lookup"><span data-stu-id="51f96-109">When the wizard displays the first server-side page and the user clicks the **Back** button, the server invokes **FinalBack** when notified of that event by the client's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="51f96-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51f96-110">Requirements</span></span>



| <span data-ttu-id="51f96-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="51f96-111">Requirement</span></span> | <span data-ttu-id="51f96-112">Value</span><span class="sxs-lookup"><span data-stu-id="51f96-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51f96-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51f96-113">Minimum supported client</span></span><br/> | <span data-ttu-id="51f96-114">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="51f96-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="51f96-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51f96-115">Minimum supported server</span></span><br/> | <span data-ttu-id="51f96-116">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="51f96-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="51f96-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51f96-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="51f96-118"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="51f96-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="51f96-119">IDL</span><span class="sxs-lookup"><span data-stu-id="51f96-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="51f96-120"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="51f96-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




