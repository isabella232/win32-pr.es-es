---
title: Mensaje de PSM_INDEXTOID (Prsht. h)
description: Toma el índice de una página de hoja de propiedades y devuelve su identificador de recurso. Puede enviar este mensaje explícitamente o utilizar la \_ macro PropSheet IndexToId.
ms.assetid: c153675a-360f-4916-aa0b-500636dd9022
keywords:
- PSM_INDEXTOID controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_INDEXTOID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643861ecb6dc11d949483defc282d6d65648bdca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079525"
---
# <a name="psm_indextoid-message"></a><span data-ttu-id="43fa3-105">Mensaje de PSM \_ INDEXTOID</span><span class="sxs-lookup"><span data-stu-id="43fa3-105">PSM\_INDEXTOID message</span></span>

<span data-ttu-id="43fa3-106">Toma el índice de una página de hoja de propiedades y devuelve su identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="43fa3-106">Takes the index of a property sheet page and returns its resource ID.</span></span> <span data-ttu-id="43fa3-107">Puede enviar este mensaje explícitamente o utilizar la macro [**PropSheet \_ IndexToId**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) .</span><span class="sxs-lookup"><span data-stu-id="43fa3-107">You can send this message explicitly or use the [**PropSheet\_IndexToId**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="43fa3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43fa3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43fa3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43fa3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43fa3-110">Índice de base cero de la página.</span><span class="sxs-lookup"><span data-stu-id="43fa3-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="43fa3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43fa3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43fa3-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="43fa3-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43fa3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43fa3-113">Return value</span></span>

<span data-ttu-id="43fa3-114">Devuelve el identificador de recurso de la página de la hoja de propiedades especificada por *wParam* si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="43fa3-114">Returns the resource ID of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="43fa3-115">De lo contrario, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="43fa3-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="43fa3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43fa3-116">Requirements</span></span>



| <span data-ttu-id="43fa3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="43fa3-117">Requirement</span></span> | <span data-ttu-id="43fa3-118">Value</span><span class="sxs-lookup"><span data-stu-id="43fa3-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="43fa3-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43fa3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="43fa3-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="43fa3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="43fa3-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43fa3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="43fa3-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="43fa3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="43fa3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43fa3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="43fa3-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="43fa3-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





