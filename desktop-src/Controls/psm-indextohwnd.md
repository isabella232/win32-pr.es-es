---
title: Mensaje de PSM_INDEXTOHWND (Prsht. h)
description: Toma el índice de una página de hoja de propiedades y devuelve su identificador de ventana. Puede enviar este mensaje explícitamente o utilizar la \_ macro PropSheet IndexToHwnd.
ms.assetid: 93b46b4c-47f9-4ce8-8797-f3d4bd5248e9
keywords:
- PSM_INDEXTOHWND controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_INDEXTOHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 788b1dd0e7312f301051d9a57fcdec43f3f2f72a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150813"
---
# <a name="psm_indextohwnd-message"></a><span data-ttu-id="fc4a6-105">Mensaje de PSM \_ INDEXTOHWND</span><span class="sxs-lookup"><span data-stu-id="fc4a6-105">PSM\_INDEXTOHWND message</span></span>

<span data-ttu-id="fc4a6-106">Toma el índice de una página de hoja de propiedades y devuelve su identificador de ventana.</span><span class="sxs-lookup"><span data-stu-id="fc4a6-106">Takes the index of a property sheet page and returns its window handle.</span></span> <span data-ttu-id="fc4a6-107">Puede enviar este mensaje explícitamente o utilizar la macro [**PropSheet \_ IndexToHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) .</span><span class="sxs-lookup"><span data-stu-id="fc4a6-107">You can send this message explicitly or use the [**PropSheet\_IndexToHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc4a6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc4a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc4a6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc4a6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc4a6-110">Índice de base cero de la página.</span><span class="sxs-lookup"><span data-stu-id="fc4a6-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="fc4a6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc4a6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc4a6-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fc4a6-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc4a6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc4a6-113">Return value</span></span>

<span data-ttu-id="fc4a6-114">Devuelve el identificador de la ventana de la página de la hoja de propiedades especificada por *wParam* si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="fc4a6-114">Returns the handle to the window of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="fc4a6-115">De lo contrario, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="fc4a6-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc4a6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc4a6-116">Requirements</span></span>



| <span data-ttu-id="fc4a6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc4a6-117">Requirement</span></span> | <span data-ttu-id="fc4a6-118">Value</span><span class="sxs-lookup"><span data-stu-id="fc4a6-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc4a6-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc4a6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fc4a6-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fc4a6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fc4a6-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc4a6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fc4a6-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc4a6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fc4a6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc4a6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc4a6-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc4a6-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





