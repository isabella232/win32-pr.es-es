---
title: IMsTscAxEvents OnIdleTimeoutNotification, método
description: Se llama cuando el usuario no ha realizado ninguna entrada del mouse o del teclado durante el período de tiempo establecido por el \_ método IMsRdpClientAdvancedSettings Put MinutesToIdleTimeout.
ms.assetid: 303f23c9-3544-4e06-93f0-3aca35d29fb5
ms.tgt_platform: multiple
keywords:
- Método OnIdleTimeoutNotification Servicios de Escritorio remoto
- Método OnIdleTimeoutNotification Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnIdleTimeoutNotification
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnIdleTimeoutNotification
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e305b0ed22e733053e33451aa35d3b8f8d6c138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676819"
---
# <a name="imstscaxeventsonidletimeoutnotification-method"></a><span data-ttu-id="e0471-106">IMsTscAxEvents:: OnIdleTimeoutNotification (método)</span><span class="sxs-lookup"><span data-stu-id="e0471-106">IMsTscAxEvents::OnIdleTimeoutNotification method</span></span>

<span data-ttu-id="e0471-107">Se llama cuando el usuario no ha realizado ninguna entrada del mouse o del teclado durante el período de tiempo establecido por el método [**IMsRdpClientAdvancedSettings::p UT \_ MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="e0471-107">Called when there has been no mouse or keyboard input by the user during the period of time set by the [**IMsRdpClientAdvancedSettings::put\_MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0471-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0471-108">Syntax</span></span>


```C++
void OnIdleTimeoutNotification();
```



## <a name="parameters"></a><span data-ttu-id="e0471-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0471-109">Parameters</span></span>

<span data-ttu-id="e0471-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e0471-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0471-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0471-111">Return value</span></span>

<span data-ttu-id="e0471-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e0471-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0471-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0471-113">Remarks</span></span>

<span data-ttu-id="e0471-114">De forma predeterminada, el valor de la propiedad [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) se establece en cero y el sistema no supervisa los tiempos de espera de inactividad.</span><span class="sxs-lookup"><span data-stu-id="e0471-114">By default, the value of the [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) property is set to zero and the system does not monitor for idle time-outs.</span></span> <span data-ttu-id="e0471-115">Este evento solo se produce si la propiedad está establecida en un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="e0471-115">This event occurs only if the property is set to a nonzero value.</span></span>

<span data-ttu-id="e0471-116">El valor de [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) se restablece automáticamente cada vez que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="e0471-116">The value of [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) is automatically reset each time the event occurs.</span></span>

<span data-ttu-id="e0471-117">Las aplicaciones pueden utilizar [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) en situaciones en las que resulta útil desconectar a un usuario. por ejemplo, en un escenario quiosco u otro terminal público.</span><span class="sxs-lookup"><span data-stu-id="e0471-117">Applications can use [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) in situations where it is useful to disconnect a user; for example, in a kiosk or other public terminal scenario.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0471-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0471-118">Requirements</span></span>



| <span data-ttu-id="e0471-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0471-119">Requirement</span></span> | <span data-ttu-id="e0471-120">Value</span><span class="sxs-lookup"><span data-stu-id="e0471-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0471-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0471-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e0471-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0471-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e0471-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0471-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e0471-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0471-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e0471-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e0471-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="e0471-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0471-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e0471-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e0471-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0471-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0471-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e0471-129">IID</span><span class="sxs-lookup"><span data-stu-id="e0471-129">IID</span></span><br/>                      | <span data-ttu-id="e0471-130">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="e0471-130">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="e0471-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0471-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0471-132">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="e0471-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





