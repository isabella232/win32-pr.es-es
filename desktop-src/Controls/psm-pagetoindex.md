---
title: Mensaje de PSM_PAGETOINDEX (Prsht. h)
description: Toma el identificador HPROPSHEETPAGE de la página de la hoja de propiedades y devuelve su índice basado en cero. Puede enviar este mensaje explícitamente o utilizar la \_ macro PropSheet PageToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_pagetoindex.htm
keywords:
- PSM_PAGETOINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_PAGETOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e3cb6688ab918da0dfae8affed36903e6dcea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658228"
---
# <a name="psm_pagetoindex-message"></a><span data-ttu-id="c3133-105">Mensaje de PSM \_ PAGETOINDEX</span><span class="sxs-lookup"><span data-stu-id="c3133-105">PSM\_PAGETOINDEX message</span></span>

<span data-ttu-id="c3133-106">Toma el identificador HPROPSHEETPAGE de la página de la hoja de propiedades y devuelve su índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="c3133-106">Takes the HPROPSHEETPAGE handle of the property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="c3133-107">Puede enviar este mensaje explícitamente o utilizar la macro [**PropSheet \_ PageToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) .</span><span class="sxs-lookup"><span data-stu-id="c3133-107">You can send this message explicitly or use the [**PropSheet\_PageToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3133-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c3133-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3133-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3133-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3133-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c3133-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c3133-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3133-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3133-112">Identificador de HPROPSHEETPAGE de la página de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c3133-112">HPROPSHEETPAGE handle to the property sheet page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3133-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c3133-113">Return value</span></span>

<span data-ttu-id="c3133-114">Devuelve el índice de base cero de la página de la hoja de propiedades especificada por *lParam* si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="c3133-114">Returns the zero-based index of the property sheet page specified by *lParam* if successful.</span></span> <span data-ttu-id="c3133-115">De lo contrario, devuelve -1.</span><span class="sxs-lookup"><span data-stu-id="c3133-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3133-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3133-116">Requirements</span></span>



| <span data-ttu-id="c3133-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3133-117">Requirement</span></span> | <span data-ttu-id="c3133-118">Value</span><span class="sxs-lookup"><span data-stu-id="c3133-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c3133-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3133-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c3133-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c3133-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c3133-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3133-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c3133-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c3133-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c3133-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3133-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3133-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3133-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





