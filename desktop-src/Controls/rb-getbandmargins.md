---
title: Mensaje de RB_GETBANDMARGINS (commctrl. h)
description: Recupera los márgenes de una banda.
ms.assetid: 262f4180-53f9-428f-9360-75b762470270
keywords:
- RB_GETBANDMARGINS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_GETBANDMARGINS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ab77c057073d9816d1310b1e8cb39fd374956b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996723"
---
# <a name="rb_getbandmargins-message"></a><span data-ttu-id="1e3a9-104">Mensaje de GETBANDMARGINS de RB \_</span><span class="sxs-lookup"><span data-stu-id="1e3a9-104">RB\_GETBANDMARGINS message</span></span>

<span data-ttu-id="1e3a9-105">Recupera los márgenes de una banda.</span><span class="sxs-lookup"><span data-stu-id="1e3a9-105">Retrieves the margins of a band.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e3a9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e3a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e3a9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e3a9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1e3a9-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1e3a9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1e3a9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e3a9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e3a9-110">Puntero a una estructura de [**márgenes**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) que recibe los márgenes recuperados.</span><span class="sxs-lookup"><span data-stu-id="1e3a9-110">Pointer to a [**MARGINS**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) structure that receives the retrieved margins.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e3a9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e3a9-111">Return value</span></span>

<span data-ttu-id="1e3a9-112">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="1e3a9-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e3a9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e3a9-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1e3a9-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="1e3a9-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="1e3a9-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1e3a9-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1e3a9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e3a9-116">Requirements</span></span>



| <span data-ttu-id="1e3a9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e3a9-117">Requirement</span></span> | <span data-ttu-id="1e3a9-118">Value</span><span class="sxs-lookup"><span data-stu-id="1e3a9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e3a9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e3a9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1e3a9-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1e3a9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e3a9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e3a9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1e3a9-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1e3a9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e3a9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e3a9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e3a9-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e3a9-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





