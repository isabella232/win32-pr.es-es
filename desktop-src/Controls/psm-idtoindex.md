---
title: Mensaje de PSM_IDTOINDEX (Prsht. h)
description: Toma el identificador de recurso de una página de hoja de propiedades y devuelve su índice basado en cero. Puede enviar este mensaje explícitamente o utilizar la \_ macro PropSheet IdToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_idtoindex.htm
keywords:
- PSM_IDTOINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_IDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f098c37ba30e33685abedf9dccd3ffc7c303acb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150817"
---
# <a name="psm_idtoindex-message"></a><span data-ttu-id="34cc9-105">Mensaje de PSM \_ IDTOINDEX</span><span class="sxs-lookup"><span data-stu-id="34cc9-105">PSM\_IDTOINDEX message</span></span>

<span data-ttu-id="34cc9-106">Toma el identificador de recurso de una página de hoja de propiedades y devuelve su índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="34cc9-106">Takes the resource ID of a property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="34cc9-107">Puede enviar este mensaje explícitamente o utilizar la macro [**PropSheet \_ IdToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) .</span><span class="sxs-lookup"><span data-stu-id="34cc9-107">You can send this message explicitly or use the [**PropSheet\_IdToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="34cc9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34cc9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34cc9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="34cc9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34cc9-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="34cc9-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="34cc9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="34cc9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34cc9-112">IDENTIFICADOR de recurso de la página.</span><span class="sxs-lookup"><span data-stu-id="34cc9-112">Resource ID of the page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34cc9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34cc9-113">Return value</span></span>

<span data-ttu-id="34cc9-114">Devuelve el índice de base cero de la página de la hoja de propiedades especificada por *lParam* si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="34cc9-114">Returns the zero-based index of the property sheet page specified by *lParam* if successful.</span></span> <span data-ttu-id="34cc9-115">De lo contrario, devuelve -1.</span><span class="sxs-lookup"><span data-stu-id="34cc9-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="34cc9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34cc9-116">Requirements</span></span>



| <span data-ttu-id="34cc9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="34cc9-117">Requirement</span></span> | <span data-ttu-id="34cc9-118">Value</span><span class="sxs-lookup"><span data-stu-id="34cc9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="34cc9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34cc9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="34cc9-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="34cc9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="34cc9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34cc9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="34cc9-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="34cc9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="34cc9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34cc9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="34cc9-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="34cc9-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





