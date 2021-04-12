---
title: Mensaje de CQPM_HANDLERSPECIFIC (Cmnquery. h)
description: Valor base utilizado para los mensajes que son privados para el controlador de consultas.
ms.assetid: c3badb89-ee4e-4317-97aa-15187b9bb3e8
ms.tgt_platform: multiple
keywords:
- CQPM_HANDLERSPECIFIC Active Directory de mensaje
topic_type:
- apiref
api_name:
- CQPM_HANDLERSPECIFIC
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed06d4bd2b33eaf6224bb72f4814dfdced5cce2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489478"
---
# <a name="cqpm_handlerspecific-message"></a><span data-ttu-id="61b46-104">CQPM \_ HANDLERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="61b46-104">CQPM\_HANDLERSPECIFIC message</span></span>

<span data-ttu-id="61b46-105">El mensaje **CQPM \_ HANDLERSPECIFIC** es el valor base que se usa para los mensajes que son privados para el controlador de consultas.</span><span class="sxs-lookup"><span data-stu-id="61b46-105">The **CQPM\_HANDLERSPECIFIC** message is the base value used for messages that are private to the query handler.</span></span> <span data-ttu-id="61b46-106">El controlador de consultas debe agregar este valor a los mensajes privados para asegurarse de que no se producen colisiones de mensajes.</span><span class="sxs-lookup"><span data-stu-id="61b46-106">The query handler should add this value to private messages to ensure that message collisions do not occur.</span></span>

## <a name="parameters"></a><span data-ttu-id="61b46-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61b46-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61b46-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="61b46-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61b46-109">Contiene datos de mensajes adicionales.</span><span class="sxs-lookup"><span data-stu-id="61b46-109">Contains additional message data.</span></span> <span data-ttu-id="61b46-110">El contenido de este parámetro se define mediante el controlador de consultas.</span><span class="sxs-lookup"><span data-stu-id="61b46-110">The content of this parameter is defined by the query handler.</span></span>

</dd> <dt>

<span data-ttu-id="61b46-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61b46-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61b46-112">Contiene datos de mensajes adicionales.</span><span class="sxs-lookup"><span data-stu-id="61b46-112">Contains additional message data.</span></span> <span data-ttu-id="61b46-113">El contenido de este parámetro se define mediante el controlador de consultas.</span><span class="sxs-lookup"><span data-stu-id="61b46-113">The content of this parameter is defined by the query handler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61b46-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61b46-114">Return value</span></span>

<span data-ttu-id="61b46-115">El identificador de consulta define el significado del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="61b46-115">The meaning of the return value is defined by the query handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="61b46-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61b46-116">Requirements</span></span>



| <span data-ttu-id="61b46-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="61b46-117">Requirement</span></span> | <span data-ttu-id="61b46-118">Value</span><span class="sxs-lookup"><span data-stu-id="61b46-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61b46-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61b46-119">Minimum supported client</span></span><br/> | <span data-ttu-id="61b46-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61b46-120">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="61b46-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61b46-121">Minimum supported server</span></span><br/> | <span data-ttu-id="61b46-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61b46-122">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="61b46-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61b46-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="61b46-124"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="61b46-124"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61b46-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="61b46-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61b46-126">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="61b46-126">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





