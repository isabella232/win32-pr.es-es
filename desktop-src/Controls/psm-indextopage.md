---
title: Mensaje de PSM_INDEXTOPAGE (Prsht. h)
description: Toma el índice de una página de hoja de propiedades y devuelve su identificador HPROPSHEETPAGE. Puede enviar este mensaje explícitamente o utilizar la \_ macro PropSheet IndexToPage.
ms.assetid: b14b35ad-bae0-4461-a90f-e2bc5e2ccfc2
keywords:
- PSM_INDEXTOPAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_INDEXTOPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38f7a5658dbd92f4208e084f1df47a4dc3582156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492131"
---
# <a name="psm_indextopage-message"></a><span data-ttu-id="0d82e-105">Mensaje de PSM \_ INDEXTOPAGE</span><span class="sxs-lookup"><span data-stu-id="0d82e-105">PSM\_INDEXTOPAGE message</span></span>

<span data-ttu-id="0d82e-106">Toma el índice de una página de hoja de propiedades y devuelve su identificador HPROPSHEETPAGE.</span><span class="sxs-lookup"><span data-stu-id="0d82e-106">Takes the index of a property sheet page and returns its HPROPSHEETPAGE handle.</span></span> <span data-ttu-id="0d82e-107">Puede enviar este mensaje explícitamente o utilizar la macro [**PropSheet \_ IndexToPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) .</span><span class="sxs-lookup"><span data-stu-id="0d82e-107">You can send this message explicitly or use the [**PropSheet\_IndexToPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d82e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d82e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d82e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d82e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d82e-110">Índice de base cero de la página.</span><span class="sxs-lookup"><span data-stu-id="0d82e-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="0d82e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d82e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d82e-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0d82e-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d82e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d82e-113">Return value</span></span>

<span data-ttu-id="0d82e-114">Devuelve el identificador HPROPSHEETPAGE de la página de la hoja de propiedades especificada por *wParam* si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="0d82e-114">Returns the HPROPSHEETPAGE handle of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="0d82e-115">De lo contrario, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="0d82e-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d82e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d82e-116">Requirements</span></span>



| <span data-ttu-id="0d82e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d82e-117">Requirement</span></span> | <span data-ttu-id="0d82e-118">Value</span><span class="sxs-lookup"><span data-stu-id="0d82e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d82e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d82e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0d82e-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0d82e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0d82e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d82e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0d82e-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d82e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0d82e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d82e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d82e-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d82e-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





