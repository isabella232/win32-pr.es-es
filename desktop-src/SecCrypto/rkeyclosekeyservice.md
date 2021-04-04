---
description: No se admite la función RKeyCloseKeyService.
ms.assetid: 3a3d41d4-d8ce-4ed8-a70b-dd3629ab7b44
title: Función RKeyCloseKeyService (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyCloseKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 3a35362876c067de011ec69a858e20150308cbd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907977"
---
# <a name="rkeyclosekeyservice-function"></a><span data-ttu-id="b1e5c-103">RKeyCloseKeyService función)</span><span class="sxs-lookup"><span data-stu-id="b1e5c-103">RKeyCloseKeyService function</span></span>

<span data-ttu-id="b1e5c-104">No se admite la función **RKeyCloseKeyService** .</span><span class="sxs-lookup"><span data-stu-id="b1e5c-104">The **RKeyCloseKeyService** function is not supported.</span></span>

<span data-ttu-id="b1e5c-105">**Windows Server 2003:** La función **RKeyCloseKeyService** cierra un identificador del servicio de claves abierto por una llamada anterior a la función [**RKeyOpenKeyService**](rkeyopenkeyservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b1e5c-105">**Windows Server 2003:** The **RKeyCloseKeyService** function closes a key service handle opened by a previous call to the [**RKeyOpenKeyService**](rkeyopenkeyservice.md) function.</span></span> <span data-ttu-id="b1e5c-106">Tenga en cuenta que este comportamiento ha cambiado con Windows Server 2003 con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="b1e5c-106">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1e5c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1e5c-107">Syntax</span></span>


```C++
ULONG RKeyCloseKeyService(
  _In_    KEYSVCC_HANDLE hKeySvcCli,
  _Inout_ void           *pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="b1e5c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1e5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1e5c-109">*hKeySvcCli* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b1e5c-109">*hKeySvcCli* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1e5c-110">Identificador [**de \_ controlador de KEYSVCC**](keysvcc-handle.md) abierto previamente por [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span><span class="sxs-lookup"><span data-stu-id="b1e5c-110">A [**KEYSVCC\_HANDLE**](keysvcc-handle.md) handle previously opened by [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span></span> <span data-ttu-id="b1e5c-111">Este valor no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="b1e5c-111">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b1e5c-112">*conservado* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b1e5c-112">*pReserved* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1e5c-113">Reservado.</span><span class="sxs-lookup"><span data-stu-id="b1e5c-113">Reserved.</span></span> <span data-ttu-id="b1e5c-114">Establezca este valor en **null**.</span><span class="sxs-lookup"><span data-stu-id="b1e5c-114">Set this value to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1e5c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1e5c-115">Return value</span></span>

<span data-ttu-id="b1e5c-116">Si la función se realiza correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b1e5c-116">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="b1e5c-117">Si se produce un error en la función, el valor devuelto es un **ULong** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="b1e5c-117">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1e5c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1e5c-118">Requirements</span></span>



| <span data-ttu-id="b1e5c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1e5c-119">Requirement</span></span> | <span data-ttu-id="b1e5c-120">Value</span><span class="sxs-lookup"><span data-stu-id="b1e5c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1e5c-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1e5c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b1e5c-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b1e5c-122">None supported</span></span><br/>                                                             |
| <span data-ttu-id="b1e5c-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1e5c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b1e5c-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1e5c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b1e5c-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1e5c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1e5c-126"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1e5c-126"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1e5c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1e5c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1e5c-128">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="b1e5c-128">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> <dt>

[<span data-ttu-id="b1e5c-129">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="b1e5c-129">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> </dl>

 

 




