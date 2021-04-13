---
title: Mensaje EM_GETIMECOMPMODE (RichEdit. h)
description: Recupera el modo del editor de métodos de entrada (IME) actual para un control Rich Edit.
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- EM_GETIMECOMPMODE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETIMECOMPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feb2f5f31831e0e292bf002f24ca4978f25753a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491806"
---
# <a name="em_getimecompmode-message"></a><span data-ttu-id="183d9-104">\_Mensaje GETIMECOMPMODE em</span><span class="sxs-lookup"><span data-stu-id="183d9-104">EM\_GETIMECOMPMODE message</span></span>

<span data-ttu-id="183d9-105">Recupera el modo del editor de métodos de entrada (IME) actual para un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="183d9-105">Retrieves the current Input Method Editor (IME) mode for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="183d9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="183d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="183d9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="183d9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="183d9-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="183d9-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="183d9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="183d9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="183d9-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="183d9-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="183d9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="183d9-111">Return value</span></span>

<span data-ttu-id="183d9-112">El valor devuelto es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="183d9-112">The return value is one of the following values.</span></span>



| <span data-ttu-id="183d9-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="183d9-113">Return code</span></span>                                                                                     | <span data-ttu-id="183d9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="183d9-114">Description</span></span>                  |
|-------------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="183d9-115"><dt>**\_NOTOPEN ICM**</dt></span><span class="sxs-lookup"><span data-stu-id="183d9-115"><dt>**ICM\_NOTOPEN**</dt></span></span> </dl>     | <span data-ttu-id="183d9-116">El IME no está abierto.</span><span class="sxs-lookup"><span data-stu-id="183d9-116">IME is not open.</span></span><br/>  |
| <dl> <span data-ttu-id="183d9-117"><dt>**\_Level3 ICM**</dt></span><span class="sxs-lookup"><span data-stu-id="183d9-117"><dt>**ICM\_LEVEL3**</dt></span></span> </dl>      | <span data-ttu-id="183d9-118">Verdadero modo insertado.</span><span class="sxs-lookup"><span data-stu-id="183d9-118">True inline mode.</span></span><br/> |
| <dl> <span data-ttu-id="183d9-119"><dt>**\_LEVEL2 ICM**</dt></span><span class="sxs-lookup"><span data-stu-id="183d9-119"><dt>**ICM\_LEVEL2**</dt></span></span> </dl>      | <span data-ttu-id="183d9-120">Nivel 2.</span><span class="sxs-lookup"><span data-stu-id="183d9-120">Level 2.</span></span><br/>          |
| <dl> <span data-ttu-id="183d9-121"><dt>**ICM \_ LEVEL2 \_ 5**</dt></span><span class="sxs-lookup"><span data-stu-id="183d9-121"><dt>**ICM\_LEVEL2\_5**</dt></span></span> </dl>   | <span data-ttu-id="183d9-122">Nivel 2,5</span><span class="sxs-lookup"><span data-stu-id="183d9-122">Level 2.5</span></span><br/>         |
| <dl> <span data-ttu-id="183d9-123"><dt>**LEVEL2 de ICM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="183d9-123"><dt>**ICM\_LEVEL2\_SUI**</dt></span></span> </dl> | <span data-ttu-id="183d9-124">Interfaz de usuario especial.</span><span class="sxs-lookup"><span data-stu-id="183d9-124">Special UI.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="183d9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="183d9-125">Requirements</span></span>



| <span data-ttu-id="183d9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="183d9-126">Requirement</span></span> | <span data-ttu-id="183d9-127">Value</span><span class="sxs-lookup"><span data-stu-id="183d9-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="183d9-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="183d9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="183d9-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="183d9-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="183d9-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="183d9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="183d9-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="183d9-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="183d9-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="183d9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="183d9-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="183d9-133"><dt>Richedit.h</dt></span></span> </dl> |



 

 





