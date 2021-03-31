---
title: Mensaje de UDM_SETBASE (commctrl. h)
description: Establece la base de base de un control de flechas. El valor base determina si la ventana relacionada muestra números en dígitos decimales o hexadecimales. Los números hexadecimales siempre están sin signo y los números decimales están firmados.
ms.assetid: c76cdec1-e73b-4b4b-89be-9a00ff2ea172
keywords:
- UDM_SETBASE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- UDM_SETBASE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6bcd7d6154b4ba732e5ffbbec889b326ec8176
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996716"
---
# <a name="udm_setbase-message"></a><span data-ttu-id="40de4-106">\_Mensaje SETBASE UDM</span><span class="sxs-lookup"><span data-stu-id="40de4-106">UDM\_SETBASE message</span></span>

<span data-ttu-id="40de4-107">Establece la base de base de un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="40de4-107">Sets the radix base for an up-down control.</span></span> <span data-ttu-id="40de4-108">El valor base determina si la ventana relacionada muestra números en dígitos decimales o hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="40de4-108">The base value determines whether the buddy window displays numbers in decimal or hexadecimal digits.</span></span> <span data-ttu-id="40de4-109">Los números hexadecimales siempre están sin signo y los números decimales están firmados.</span><span class="sxs-lookup"><span data-stu-id="40de4-109">Hexadecimal numbers are always unsigned, and decimal numbers are signed.</span></span>

## <a name="parameters"></a><span data-ttu-id="40de4-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40de4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40de4-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="40de4-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40de4-112">Nuevo valor base para el control.</span><span class="sxs-lookup"><span data-stu-id="40de4-112">New base value for the control.</span></span> <span data-ttu-id="40de4-113">Este parámetro puede ser 10 para decimal o 16 para hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="40de4-113">This parameter can be 10 for decimal or 16 for hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="40de4-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="40de4-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="40de4-115">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="40de4-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40de4-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40de4-116">Return value</span></span>

<span data-ttu-id="40de4-117">El valor devuelto es el valor base anterior.</span><span class="sxs-lookup"><span data-stu-id="40de4-117">The return value is the previous base value.</span></span> <span data-ttu-id="40de4-118">Si se proporciona una base no válida, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="40de4-118">If an invalid base is given, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="40de4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40de4-119">Requirements</span></span>



| <span data-ttu-id="40de4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="40de4-120">Requirement</span></span> | <span data-ttu-id="40de4-121">Value</span><span class="sxs-lookup"><span data-stu-id="40de4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40de4-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40de4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="40de4-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="40de4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="40de4-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40de4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="40de4-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="40de4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="40de4-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40de4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="40de4-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="40de4-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





