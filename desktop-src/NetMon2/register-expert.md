---
description: El experto debe implementar la función Register Expert. Monitor de red llama a la función Register Expert para obtener información sobre el experto.
ms.assetid: 58cfe525-99b1-40ce-b8d8-fa1c62a20c40
title: Registrar función de devolución de llamada experta (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 085d5c59b17b10949ad39d07354906f40e123988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908697"
---
# <a name="register-expert-callback-function"></a><span data-ttu-id="9ae63-104">Registrar función de devolución de llamada experta</span><span class="sxs-lookup"><span data-stu-id="9ae63-104">Register Expert callback function</span></span>

<span data-ttu-id="9ae63-105">El experto debe implementar la función **Register** Expert.</span><span class="sxs-lookup"><span data-stu-id="9ae63-105">The expert must implement the **Register** expert function.</span></span> <span data-ttu-id="9ae63-106">Monitor de red llama a la función **Register** Expert para obtener información sobre el experto.</span><span class="sxs-lookup"><span data-stu-id="9ae63-106">Network Monitor calls the **Register** expert function to obtain information about the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ae63-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ae63-107">Syntax</span></span>


```C++
BOOL WINAPI Register(
  _Inout_ PEXPERTENUMINFO pExpertInfo
);
```



## <a name="parameters"></a><span data-ttu-id="9ae63-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ae63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ae63-109">*pExpertInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9ae63-109">*pExpertInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ae63-110">Puntero a una estructura [**EXPERTENUMINFO**](expertenuminfo.md) que monitor de red asigna.</span><span class="sxs-lookup"><span data-stu-id="9ae63-110">Pointer to an [**EXPERTENUMINFO**](expertenuminfo.md) structure that Network Monitor allocates.</span></span> <span data-ttu-id="9ae63-111">El experto rellena la estructura con toda la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="9ae63-111">The expert fills in the structure with all requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ae63-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ae63-112">Return value</span></span>

<span data-ttu-id="9ae63-113">Si la función es correcta, el valor devuelto es **true** y la función devuelve la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="9ae63-113">If the function is successful, the return value is **TRUE**, and the function returns the requested information.</span></span>

<span data-ttu-id="9ae63-114">Si la función no se realiza correctamente, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="9ae63-114">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ae63-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ae63-115">Remarks</span></span>

<span data-ttu-id="9ae63-116">El miembro de la **versión** de la estructura [**EXPERTENUMINFO**](expertenuminfo.md) debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9ae63-116">The **Version** member of the [**EXPERTENUMINFO**](expertenuminfo.md) structure must be zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ae63-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ae63-117">Requirements</span></span>



| <span data-ttu-id="9ae63-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ae63-118">Requirement</span></span> | <span data-ttu-id="9ae63-119">Value</span><span class="sxs-lookup"><span data-stu-id="9ae63-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9ae63-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ae63-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9ae63-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9ae63-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9ae63-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ae63-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9ae63-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9ae63-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9ae63-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ae63-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ae63-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ae63-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




