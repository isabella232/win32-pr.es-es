---
description: Establece el título y el subtítulo que aparecen en el encabezado del asistente. En general, el cliente mostrará el encabezado sobre el código HTML y debajo de la barra de título.
title: Método WebWizardHost. SetHeaderText (Shldisp. h)
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
ms.openlocfilehash: 92e23fab94cfedd8bbc62e31086759af48238a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985787"
---
# <a name="webwizardhostsetheadertext-method"></a><span data-ttu-id="388b4-104">WebWizardHost. SetHeaderText, método</span><span class="sxs-lookup"><span data-stu-id="388b4-104">WebWizardHost.SetHeaderText method</span></span>

<span data-ttu-id="388b4-105">Establece el título y el subtítulo que aparecen en el encabezado del asistente.</span><span class="sxs-lookup"><span data-stu-id="388b4-105">Sets the title and subtitle that appear in the wizard header.</span></span> <span data-ttu-id="388b4-106">En general, el cliente mostrará el encabezado sobre el código HTML y debajo de la barra de título.</span><span class="sxs-lookup"><span data-stu-id="388b4-106">In general, the client will display the header above the HTML and below the title bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="388b4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="388b4-107">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a><span data-ttu-id="388b4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="388b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="388b4-109">*bstrHeaderTitle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="388b4-109">*bstrHeaderTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="388b4-110">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="388b4-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="388b4-111">Cadena que contiene el título.</span><span class="sxs-lookup"><span data-stu-id="388b4-111">String containing the title.</span></span>

</dd> <dt>

<span data-ttu-id="388b4-112">*bstrHeaderSubtitle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="388b4-112">*bstrHeaderSubtitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="388b4-113">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="388b4-113">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="388b4-114">Cadena que contiene el subtítulo.</span><span class="sxs-lookup"><span data-stu-id="388b4-114">String containing the subtitle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="388b4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="388b4-115">Requirements</span></span>



| <span data-ttu-id="388b4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="388b4-116">Requirement</span></span> | <span data-ttu-id="388b4-117">Value</span><span class="sxs-lookup"><span data-stu-id="388b4-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="388b4-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="388b4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="388b4-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="388b4-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="388b4-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="388b4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="388b4-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="388b4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="388b4-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="388b4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="388b4-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="388b4-123"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="388b4-124">IDL</span><span class="sxs-lookup"><span data-stu-id="388b4-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="388b4-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="388b4-125"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 
