---
title: Método BasicDevice.add_ConnectionStatusChanged
description: Registra un controlador de eventos para el evento ConnectionStatusChanged. | Método BasicDevice.add_ConnectionStatusChanged
ms.assetid: FFAA0981-508C-4300-9CA9-24C6AFC1183D
keywords:
- método add_ConnectionStatusChanged API de streaming multimedia
- método add_ConnectionStatusChanged API de streaming multimedia, interfaz BasicDevice
- BasicDevice interface media streaming API, método add_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- BasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61a36e46d554a953ecd061ccf2396d33b0578d8f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105707663"
---
# <a name="basicdeviceadd_connectionstatuschanged-method"></a><span data-ttu-id="d874a-107">BasicDevice. Add \_ ConnectionStatusChanged (método)</span><span class="sxs-lookup"><span data-stu-id="d874a-107">BasicDevice.add\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="d874a-108">Registra un controlador de eventos para el evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="d874a-108">Registers an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="d874a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d874a-109">Syntax</span></span>


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a><span data-ttu-id="d874a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d874a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d874a-111">*controlador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d874a-111">*handler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d874a-112">Función de controlador de eventos [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d874a-112">A [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) event handler function.</span></span>

</dd> <dt>

<span data-ttu-id="d874a-113">*token* \[ de out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d874a-113">*token* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d874a-114">Referencia a un token que se puede usar para anular el registro del controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="d874a-114">Reference to a token that can be used to unregister the event handler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d874a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d874a-115">Return value</span></span>

<span data-ttu-id="d874a-116">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d874a-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d874a-117">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="d874a-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d874a-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d874a-118">Return code</span></span>                                                                          | <span data-ttu-id="d874a-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="d874a-119">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d874a-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d874a-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d874a-121">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="d874a-121">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d874a-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d874a-122">Remarks</span></span>

<span data-ttu-id="d874a-123">Para anular el registro del controlador de eventos registrado por este método, pase el valor del *token* al método [**Remove \_ ConnectionStatusChanged**](basicdevice-remove-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="d874a-123">To unregister the event handler that was registered by this method, pass the *token* value to the [**remove\_ConnectionStatusChanged**](basicdevice-remove-connectionstatuschanged.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="d874a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d874a-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="d874a-125">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d874a-125">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span></span>
</dt> </dl>

 

