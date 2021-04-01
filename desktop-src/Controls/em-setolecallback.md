---
title: Mensaje EM_SETOLECALLBACK (RichEdit. h)
description: Proporciona un control de edición enriquecido a un objeto IRichEditOleCallback que el control usa para obtener recursos e información relacionados con OLE del cliente.
ms.assetid: bd1f8048-214c-4ac6-b826-bedabb1aaee5
keywords:
- EM_SETOLECALLBACK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETOLECALLBACK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfc54db112bba42fc3d51b2e328fc7641990c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996561"
---
# <a name="em_setolecallback-message"></a><span data-ttu-id="a499d-104">\_Mensaje SETOLECALLBACK em</span><span class="sxs-lookup"><span data-stu-id="a499d-104">EM\_SETOLECALLBACK message</span></span>

<span data-ttu-id="a499d-105">Proporciona un control de edición enriquecido a un objeto [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) que el control usa para obtener recursos e información relacionados con OLE del cliente.</span><span class="sxs-lookup"><span data-stu-id="a499d-105">Gives a rich edit control an [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) object that the control uses to get OLE-related resources and information from the client.</span></span>

## <a name="parameters"></a><span data-ttu-id="a499d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a499d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a499d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a499d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a499d-108">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a499d-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a499d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a499d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a499d-110">Puntero a un objeto [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) .</span><span class="sxs-lookup"><span data-stu-id="a499d-110">Pointer to an [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) object.</span></span> <span data-ttu-id="a499d-111">El control llama al método [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) para el objeto antes de devolver.</span><span class="sxs-lookup"><span data-stu-id="a499d-111">The control calls the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method for the object before returning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a499d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a499d-112">Return value</span></span>

<span data-ttu-id="a499d-113">Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="a499d-113">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a499d-114">Si se produce un error en la operación, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="a499d-114">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a499d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a499d-115">Requirements</span></span>



| <span data-ttu-id="a499d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a499d-116">Requirement</span></span> | <span data-ttu-id="a499d-117">Value</span><span class="sxs-lookup"><span data-stu-id="a499d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a499d-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a499d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a499d-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a499d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a499d-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a499d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a499d-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a499d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a499d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a499d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a499d-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a499d-123"><dt>Richedit.h</dt></span></span> </dl> |



 

