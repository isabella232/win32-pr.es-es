---
title: Mensaje de PSM_HWNDTOINDEX (Prsht. h)
description: Toma el identificador de ventana de la página de la hoja de propiedades y devuelve su índice basado en cero. Puede enviar este mensaje explícitamente o utilizar la \_ macro PropSheet HwndToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_hwndtoindex.htm
keywords:
- PSM_HWNDTOINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_HWNDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6632d331a6f271e339663a23210d0b399fb669b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150458"
---
# <a name="psm_hwndtoindex-message"></a><span data-ttu-id="b5417-105">Mensaje de PSM \_ HWNDTOINDEX</span><span class="sxs-lookup"><span data-stu-id="b5417-105">PSM\_HWNDTOINDEX message</span></span>

<span data-ttu-id="b5417-106">Toma el identificador de ventana de la página de la hoja de propiedades y devuelve su índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="b5417-106">Takes the window handle of the property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="b5417-107">Puede enviar este mensaje explícitamente o utilizar la macro [**PropSheet \_ HwndToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) .</span><span class="sxs-lookup"><span data-stu-id="b5417-107">You can send this message explicitly or use the [**PropSheet\_HwndToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5417-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5417-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5417-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5417-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5417-110">Identificador de la ventana de la página.</span><span class="sxs-lookup"><span data-stu-id="b5417-110">Handle to the page's window.</span></span>

</dd> <dt>

<span data-ttu-id="b5417-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5417-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5417-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b5417-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5417-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5417-113">Return value</span></span>

<span data-ttu-id="b5417-114">Devuelve el índice de base cero de la página de la hoja de propiedades especificada por *wParam* si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="b5417-114">Returns the zero-based index of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="b5417-115">De lo contrario, devuelve -1.</span><span class="sxs-lookup"><span data-stu-id="b5417-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5417-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5417-116">Requirements</span></span>



| <span data-ttu-id="b5417-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5417-117">Requirement</span></span> | <span data-ttu-id="b5417-118">Value</span><span class="sxs-lookup"><span data-stu-id="b5417-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5417-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5417-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b5417-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b5417-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b5417-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5417-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b5417-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5417-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b5417-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5417-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5417-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5417-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





