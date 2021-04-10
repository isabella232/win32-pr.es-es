---
title: Mensaje de PSM_UNCHANGED (Prsht. h)
description: Informa a una hoja de propiedades de que la información de una página ha revertido al estado guardado anteriormente. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ sin cambios.
ms.assetid: 61c15dec-40d0-4720-a117-4eed765c8819
keywords:
- PSM_UNCHANGED controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_UNCHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d6216f94afd610bb49710a3e84b4c21a673f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274546"
---
# <a name="psm_unchanged-message"></a><span data-ttu-id="fb5a8-105">Mensaje de PSM \_ sin cambios</span><span class="sxs-lookup"><span data-stu-id="fb5a8-105">PSM\_UNCHANGED message</span></span>

<span data-ttu-id="fb5a8-106">Informa a una hoja de propiedades de que la información de una página ha revertido al estado guardado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="fb5a8-106">Informs a property sheet that information in a page has reverted to the previously saved state.</span></span> <span data-ttu-id="fb5a8-107">Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ sin cambios**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) .</span><span class="sxs-lookup"><span data-stu-id="fb5a8-107">You can send this message explicitly or by using the [**PropSheet\_UnChanged**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fb5a8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb5a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb5a8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fb5a8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb5a8-110">Identificador de la página que se ha revertido al estado guardado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="fb5a8-110">Handle to the page that has reverted to the previously saved state.</span></span>

</dd> <dt>

<span data-ttu-id="fb5a8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fb5a8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb5a8-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fb5a8-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb5a8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb5a8-113">Return value</span></span>

<span data-ttu-id="fb5a8-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fb5a8-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb5a8-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb5a8-115">Remarks</span></span>

<span data-ttu-id="fb5a8-116">La hoja de propiedades deshabilita el botón **aplicar** si ninguna otra página tiene cambios registrados con la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="fb5a8-116">The property sheet disables the **Apply** button if no other pages have registered changes with the property sheet.</span></span>

> [!Note]  
> <span data-ttu-id="fb5a8-117">Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="fb5a8-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fb5a8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb5a8-118">Requirements</span></span>



| <span data-ttu-id="fb5a8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb5a8-119">Requirement</span></span> | <span data-ttu-id="fb5a8-120">Value</span><span class="sxs-lookup"><span data-stu-id="fb5a8-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb5a8-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb5a8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fb5a8-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fb5a8-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fb5a8-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb5a8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fb5a8-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fb5a8-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fb5a8-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb5a8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb5a8-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb5a8-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





