---
title: Mensaje EM_GETOLEINTERFACE (RichEdit. h)
description: Recupera un objeto IRichEditOle que un cliente puede utilizar para tener acceso a la funcionalidad del modelo de objetos componentes (COM) de un control Rich Edit.
ms.assetid: fa462c7b-29b9-4694-b7ad-6068c69ffb76
keywords:
- EM_GETOLEINTERFACE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETOLEINTERFACE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d7557d40c6dcec38ce629d949a8db9915714821
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150665"
---
# <a name="em_getoleinterface-message"></a><span data-ttu-id="dd541-104">\_Mensaje GETOLEINTERFACE em</span><span class="sxs-lookup"><span data-stu-id="dd541-104">EM\_GETOLEINTERFACE message</span></span>

<span data-ttu-id="dd541-105">Recupera un objeto [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) que un cliente puede utilizar para tener acceso a la funcionalidad del modelo de objetos componentes (com) de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="dd541-105">Retrieves an [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) object that a client can use to access a rich edit control's Component Object Model (COM) functionality.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd541-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd541-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd541-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd541-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd541-108">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="dd541-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dd541-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd541-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd541-110">Puntero a un puntero que recibe el objeto [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) .</span><span class="sxs-lookup"><span data-stu-id="dd541-110">Pointer to a pointer that receives the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) object.</span></span> <span data-ttu-id="dd541-111">El control llama al método [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) para el objeto antes de devolver, por lo que la aplicación que realiza la llamada debe llamar al método [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) cuando se realiza con el objeto.</span><span class="sxs-lookup"><span data-stu-id="dd541-111">The control calls the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method for the object before returning, so the calling application must call the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) method when it is done with the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd541-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd541-112">Return value</span></span>

<span data-ttu-id="dd541-113">Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="dd541-113">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="dd541-114">Si se produce un error en la operación, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="dd541-114">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd541-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd541-115">Requirements</span></span>



| <span data-ttu-id="dd541-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd541-116">Requirement</span></span> | <span data-ttu-id="dd541-117">Value</span><span class="sxs-lookup"><span data-stu-id="dd541-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd541-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd541-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dd541-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dd541-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd541-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd541-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dd541-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd541-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd541-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd541-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd541-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd541-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd541-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd541-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd541-125">**IRichEditOle**</span><span class="sxs-lookup"><span data-stu-id="dd541-125">**IRichEditOle**</span></span>](/windows/desktop/api/Richole/nn-richole-iricheditole)
</dt> </dl>

 

