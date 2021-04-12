---
title: Mensaje de IPM_SETADDRESS (commctrl. h)
description: Establece los valores de dirección de los cuatro campos en el control de dirección IP.
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- IPM_SETADDRESS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- IPM_SETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e8e4fa69791f93094d24f990ad62207cad33dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150547"
---
# <a name="ipm_setaddress-message"></a><span data-ttu-id="45701-104">\_Mensaje SETADDRESS de IPM</span><span class="sxs-lookup"><span data-stu-id="45701-104">IPM\_SETADDRESS message</span></span>

<span data-ttu-id="45701-105">Establece los valores de dirección de los cuatro campos en el control de dirección IP.</span><span class="sxs-lookup"><span data-stu-id="45701-105">Sets the address values for all four fields in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="45701-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45701-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45701-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="45701-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="45701-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="45701-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="45701-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="45701-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45701-110">Valor **DWORD** que contiene la nueva dirección.</span><span class="sxs-lookup"><span data-stu-id="45701-110">A **DWORD** value that contains the new address.</span></span> <span data-ttu-id="45701-111">El valor del campo 3 se incluye en los bits 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="45701-111">The field 3 value is contained in bits 0 through 7.</span></span> <span data-ttu-id="45701-112">El valor del campo 2 se incluye en los bits 8 a 15.</span><span class="sxs-lookup"><span data-stu-id="45701-112">The field 2 value is contained in bits 8 through 15.</span></span> <span data-ttu-id="45701-113">El valor del campo 1 se incluye en los bits 16 a 23.</span><span class="sxs-lookup"><span data-stu-id="45701-113">The field 1 value is contained in bits 16 through 23.</span></span> <span data-ttu-id="45701-114">El valor del campo 0 está incluido en los bits 24 a 31.</span><span class="sxs-lookup"><span data-stu-id="45701-114">The field 0 value is contained in bits 24 through 31.</span></span> <span data-ttu-id="45701-115">La macro [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) también se puede usar para crear la información de dirección.</span><span class="sxs-lookup"><span data-stu-id="45701-115">The [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) macro can also be used to create the address information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45701-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45701-116">Return value</span></span>

<span data-ttu-id="45701-117">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="45701-117">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="45701-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45701-118">Remarks</span></span>

<span data-ttu-id="45701-119">Este mensaje no genera una notificación [**de \_ FIELDCHANGED de IPN**](ipn-fieldchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="45701-119">This message does not generate an [**IPN\_FIELDCHANGED**](ipn-fieldchanged.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="45701-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45701-120">Requirements</span></span>



| <span data-ttu-id="45701-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="45701-121">Requirement</span></span> | <span data-ttu-id="45701-122">Value</span><span class="sxs-lookup"><span data-stu-id="45701-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45701-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45701-123">Minimum supported client</span></span><br/> | <span data-ttu-id="45701-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="45701-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="45701-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45701-125">Minimum supported server</span></span><br/> | <span data-ttu-id="45701-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="45701-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="45701-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45701-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="45701-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="45701-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





