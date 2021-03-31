---
title: Mensaje EM_GETAUTOURLDETECT (RichEdit. h)
description: Indica si la detección de dirección URL automática está activada en el control Rich Edit.
ms.assetid: f723f15c-bf8f-41ab-aef0-bd8f2c0b9e5d
keywords:
- EM_GETAUTOURLDETECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETAUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e68e4f2991c5f8780cb587594289674e07ec992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079457"
---
# <a name="em_getautourldetect-message"></a><span data-ttu-id="1041f-104">\_Mensaje GETAUTOURLDETECT em</span><span class="sxs-lookup"><span data-stu-id="1041f-104">EM\_GETAUTOURLDETECT message</span></span>

<span data-ttu-id="1041f-105">Indica si la detección de dirección URL automática está activada en el control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="1041f-105">Indicates whether the auto URL detection is turned on in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1041f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1041f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1041f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1041f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1041f-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1041f-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1041f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1041f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1041f-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1041f-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1041f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1041f-111">Return value</span></span>

<span data-ttu-id="1041f-112">Si la detección de dirección URL automática está activa, el valor devuelto es 1.</span><span class="sxs-lookup"><span data-stu-id="1041f-112">If auto-URL detection is active, the return value is 1.</span></span>

<span data-ttu-id="1041f-113">Si la detección de dirección URL automática está inactiva, el valor devuelto es 0.</span><span class="sxs-lookup"><span data-stu-id="1041f-113">If auto-URL detection is inactive, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="1041f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1041f-114">Remarks</span></span>

<span data-ttu-id="1041f-115">Cuando la detección de dirección URL automática está activada, Microsoft Rich Edit comprueba constantemente el texto escrito para obtener una dirección URL válida.</span><span class="sxs-lookup"><span data-stu-id="1041f-115">When auto URL detection is on, Microsoft Rich Edit is constantly checking typed text for a valid URL.</span></span> <span data-ttu-id="1041f-116">Rich Edit reconoce las direcciones URL que comienzan con estos prefijos:</span><span class="sxs-lookup"><span data-stu-id="1041f-116">Rich Edit recognizes URLs that start with these prefixes:</span></span>

-   <span data-ttu-id="1041f-117">http:</span><span class="sxs-lookup"><span data-stu-id="1041f-117">http:</span></span>
-   <span data-ttu-id="1041f-118">file:</span><span class="sxs-lookup"><span data-stu-id="1041f-118">file:</span></span>
-   <span data-ttu-id="1041f-119">mailto:</span><span class="sxs-lookup"><span data-stu-id="1041f-119">mailto:</span></span>
-   <span data-ttu-id="1041f-120">FTP</span><span class="sxs-lookup"><span data-stu-id="1041f-120">ftp:</span></span>
-   <span data-ttu-id="1041f-121">https</span><span class="sxs-lookup"><span data-stu-id="1041f-121">https:</span></span>
-   <span data-ttu-id="1041f-122">:/</span><span class="sxs-lookup"><span data-stu-id="1041f-122">gopher:</span></span>
-   <span data-ttu-id="1041f-123">NNTP</span><span class="sxs-lookup"><span data-stu-id="1041f-123">nntp:</span></span>
-   <span data-ttu-id="1041f-124">prospero:</span><span class="sxs-lookup"><span data-stu-id="1041f-124">prospero:</span></span>
-   <span data-ttu-id="1041f-125">habitualmente</span><span class="sxs-lookup"><span data-stu-id="1041f-125">telnet:</span></span>
-   <span data-ttu-id="1041f-126">Reportaje</span><span class="sxs-lookup"><span data-stu-id="1041f-126">news:</span></span>
-   <span data-ttu-id="1041f-127">WAIS</span><span class="sxs-lookup"><span data-stu-id="1041f-127">wais:</span></span>
-   <span data-ttu-id="1041f-128">Outlook</span><span class="sxs-lookup"><span data-stu-id="1041f-128">outlook:</span></span>

<span data-ttu-id="1041f-129">La edición enriquecida también reconoce los nombres de ruta de acceso estándar que comienzan por \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="1041f-129">Rich Edit also recognizes standard path names that start with \\\\.</span></span> <span data-ttu-id="1041f-130">Cuando Rich Edit localiza una dirección URL, cambia el color del texto de la dirección URL, subraya el texto y notifica al cliente mediante el [ \_ vínculo en](en-link.md).</span><span class="sxs-lookup"><span data-stu-id="1041f-130">When Rich Edit locates a URL, it changes the URL text color, underlines the text, and notifies the client using [EN\_LINK](en-link.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1041f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1041f-131">Requirements</span></span>



| <span data-ttu-id="1041f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1041f-132">Requirement</span></span> | <span data-ttu-id="1041f-133">Value</span><span class="sxs-lookup"><span data-stu-id="1041f-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1041f-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1041f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1041f-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1041f-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1041f-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1041f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1041f-137">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1041f-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1041f-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1041f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1041f-139"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1041f-139"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1041f-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="1041f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1041f-141">EN \_ vínculo</span><span class="sxs-lookup"><span data-stu-id="1041f-141">EN\_LINK</span></span>](en-link.md)
</dt> </dl>

 

 





