---
title: Mensaje de IPM_GETADDRESS (commctrl. h)
description: Obtiene los valores de dirección de los cuatro campos del control de dirección IP.
ms.assetid: 4fe68d45-7d7f-46da-a110-65f899b3c393
keywords:
- IPM_GETADDRESS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- IPM_GETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 426e9c76712701b2f4e108679133be23eb700687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996648"
---
# <a name="ipm_getaddress-message"></a><span data-ttu-id="54632-104">Mensaje de GETADDRESS de IPM \_</span><span class="sxs-lookup"><span data-stu-id="54632-104">IPM\_GETADDRESS message</span></span>

<span data-ttu-id="54632-105">Obtiene los valores de dirección de los cuatro campos del control de dirección IP.</span><span class="sxs-lookup"><span data-stu-id="54632-105">Gets the address values for all four fields in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="54632-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54632-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54632-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54632-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="54632-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="54632-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="54632-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54632-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54632-110">Un puntero a un valor **DWORD** que recibe la dirección.</span><span class="sxs-lookup"><span data-stu-id="54632-110">A pointer to a **DWORD** value that receives the address.</span></span> <span data-ttu-id="54632-111">El valor del campo 3 se incluirá en los bits 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="54632-111">The field 3 value will be contained in bits 0 through 7.</span></span> <span data-ttu-id="54632-112">El valor del campo 2 estará incluido en los bits 8 a 15.</span><span class="sxs-lookup"><span data-stu-id="54632-112">The field 2 value will be contained in bits 8 through 15.</span></span> <span data-ttu-id="54632-113">El valor del campo 1 se incluirá en los bits 16 a 23.</span><span class="sxs-lookup"><span data-stu-id="54632-113">The field 1 value will be contained in bits 16 through 23.</span></span> <span data-ttu-id="54632-114">El valor del campo 0 se incluirá en los bits 24 a 31.</span><span class="sxs-lookup"><span data-stu-id="54632-114">The field 0 value will be contained in bits 24 through 31.</span></span> <span data-ttu-id="54632-115">Las [**primeras \_**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)macros IPAddress, [**Second \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress), [**tercera \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)y [**cuarto \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) también se pueden usar para extraer la información de dirección.</span><span class="sxs-lookup"><span data-stu-id="54632-115">The [**FIRST\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress), [**SECOND\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress), [**THIRD\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress), and [**FOURTH\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) macros can also be used to extract the address information.</span></span> <span data-ttu-id="54632-116">Se devolverá cero como dirección para los campos en blanco.</span><span class="sxs-lookup"><span data-stu-id="54632-116">Zero will be returned as the address for any blank fields.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54632-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54632-117">Return value</span></span>

<span data-ttu-id="54632-118">Devuelve el número de campos que no están en blanco.</span><span class="sxs-lookup"><span data-stu-id="54632-118">Returns the number of nonblank fields.</span></span>

## <a name="requirements"></a><span data-ttu-id="54632-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54632-119">Requirements</span></span>



| <span data-ttu-id="54632-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="54632-120">Requirement</span></span> | <span data-ttu-id="54632-121">Value</span><span class="sxs-lookup"><span data-stu-id="54632-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54632-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54632-122">Minimum supported client</span></span><br/> | <span data-ttu-id="54632-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="54632-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54632-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54632-124">Minimum supported server</span></span><br/> | <span data-ttu-id="54632-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="54632-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54632-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54632-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="54632-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="54632-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





