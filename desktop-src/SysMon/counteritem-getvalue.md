---
title: Método de contraelemento. GetValue
description: Recupera el último valor del contador.
ms.assetid: cf50d878-a119-42b0-bc59-b0e37ed15321
keywords:
- Método GetValue SysMon
- GetValue (método) SysMon, contraitem (clase)
- Clase de contraelemento SysMon, método GetValue
topic_type:
- apiref
api_name:
- CounterItem.GetValue
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e40950ce4a8bf24a6a4301db133779b34ce4ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666049"
---
# <a name="counteritemgetvalue-method"></a><span data-ttu-id="b2292-106">Método de contraelemento. GetValue</span><span class="sxs-lookup"><span data-stu-id="b2292-106">CounterItem.GetValue method</span></span>

<span data-ttu-id="b2292-107">Recupera el último valor del contador.</span><span class="sxs-lookup"><span data-stu-id="b2292-107">Retrieves the last value of the counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2292-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2292-108">Syntax</span></span>


```VB
CounterItem.GetValue( _
  ByRef value As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="b2292-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2292-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2292-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b2292-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2292-111">Último valor muestreado del contador.</span><span class="sxs-lookup"><span data-stu-id="b2292-111">Last sampled value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="b2292-112">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b2292-112">*status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2292-113">Indica si el valor es válido.</span><span class="sxs-lookup"><span data-stu-id="b2292-113">Indicates if the value is valid.</span></span>



| <span data-ttu-id="b2292-114">Value</span><span class="sxs-lookup"><span data-stu-id="b2292-114">Value</span></span>                                                                                              | <span data-ttu-id="b2292-115">Significado</span><span class="sxs-lookup"><span data-stu-id="b2292-115">Meaning</span></span>                            |
|----------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="b2292-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b2292-116"><dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b2292-117">El valor es válido.</span><span class="sxs-lookup"><span data-stu-id="b2292-117">The value is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="b2292-118"><dt>0xC0000BBA (3221228474)</dt></span><span class="sxs-lookup"><span data-stu-id="b2292-118"><dt>0xC0000BBA (3221228474)</dt></span></span> </dl> | <span data-ttu-id="b2292-119">El valor no es válido.</span><span class="sxs-lookup"><span data-stu-id="b2292-119">The value is not valid.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2292-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2292-120">Return value</span></span>

<span data-ttu-id="b2292-121">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b2292-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2292-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2292-122">Remarks</span></span>

<span data-ttu-id="b2292-123">Si el origen de los datos del contador es de un archivo de registro, el valor es el último valor de contador del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="b2292-123">If the source of the counter data is from a log file, the value is the last counter value in the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2292-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2292-124">Requirements</span></span>



| <span data-ttu-id="b2292-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2292-125">Requirement</span></span> | <span data-ttu-id="b2292-126">Value</span><span class="sxs-lookup"><span data-stu-id="b2292-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2292-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2292-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b2292-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b2292-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b2292-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2292-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b2292-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b2292-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b2292-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b2292-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2292-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="b2292-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2292-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2292-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2292-134">**Elemento de**</span><span class="sxs-lookup"><span data-stu-id="b2292-134">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="b2292-135">**Elemento de GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="b2292-135">**CounterItem.GetStatistics**</span></span>](counteritem-getstatistics.md)
</dt> <dt>

[<span data-ttu-id="b2292-136">**Valor de contraitem.**</span><span class="sxs-lookup"><span data-stu-id="b2292-136">**CounterItem.Value**</span></span>](counteritem-value.md)
</dt> </dl>

 

 





