---
description: Establece el título y el subtítulo que aparecen en el encabezado del asistente. En general, el cliente mostrará el encabezado encima del CÓDIGO HTML y debajo de la barra de título.
title: Método WebWizardHost.SetHeaderText (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetHeaderText
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: e627de44-9929-4e08-9fd9-ca22743f434a
ms.openlocfilehash: d524f9ae6d1031d518e237d393bbb1dc0d35b2bd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841836"
---
# <a name="webwizardhostsetheadertext-method"></a><span data-ttu-id="7a772-104">Método WebWizardHost.SetHeaderText</span><span class="sxs-lookup"><span data-stu-id="7a772-104">WebWizardHost.SetHeaderText method</span></span>

<span data-ttu-id="7a772-105">Establece el título y el subtítulo que aparecen en el encabezado del asistente.</span><span class="sxs-lookup"><span data-stu-id="7a772-105">Sets the title and subtitle that appear in the wizard header.</span></span> <span data-ttu-id="7a772-106">En general, el cliente mostrará el encabezado encima del CÓDIGO HTML y debajo de la barra de título.</span><span class="sxs-lookup"><span data-stu-id="7a772-106">In general, the client will display the header above the HTML and below the title bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a772-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a772-107">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a><span data-ttu-id="7a772-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a772-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a772-109">*bstrHeaderTitle* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7a772-109">*bstrHeaderTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a772-110">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="7a772-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="7a772-111">Cadena que contiene el título.</span><span class="sxs-lookup"><span data-stu-id="7a772-111">String containing the title.</span></span>

</dd> <dt>

<span data-ttu-id="7a772-112">*bstrHeaderSubtitle* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7a772-112">*bstrHeaderSubtitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a772-113">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="7a772-113">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="7a772-114">Cadena que contiene el subtítulo.</span><span class="sxs-lookup"><span data-stu-id="7a772-114">String containing the subtitle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a772-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a772-115">Requirements</span></span>



| <span data-ttu-id="7a772-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a772-116">Requirement</span></span> | <span data-ttu-id="7a772-117">Value</span><span class="sxs-lookup"><span data-stu-id="7a772-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a772-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a772-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7a772-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7a772-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7a772-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a772-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7a772-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7a772-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7a772-122">Header</span><span class="sxs-lookup"><span data-stu-id="7a772-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a772-123"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="7a772-123"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7a772-124">Idl</span><span class="sxs-lookup"><span data-stu-id="7a772-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7a772-125"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="7a772-125"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 
