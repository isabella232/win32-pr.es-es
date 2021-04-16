---
title: IMsTscAxEvents OnAutoReconnecting2, método
description: Se llama cuando un cliente está en el proceso de volver a conectar automáticamente una sesión con Escritorio remoto un servidor host de sesión de escritorio remoto (host de sesión de RD). | IMsTscAxEvents OnAutoReconnecting2, método
ms.assetid: 20F69798-5397-440C-9D0D-45AE417623A7
ms.tgt_platform: multiple
keywords:
- Método OnAutoReconnecting2 Servicios de Escritorio remoto
- Método OnAutoReconnecting2 Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnAutoReconnecting2
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901bb196922d1772782ab7f1c911c96573c88b36
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689814"
---
# <a name="imstscaxeventsonautoreconnecting2-method"></a><span data-ttu-id="e9daa-107">IMsTscAxEvents:: OnAutoReconnecting2 (método)</span><span class="sxs-lookup"><span data-stu-id="e9daa-107">IMsTscAxEvents::OnAutoReconnecting2 method</span></span>

<span data-ttu-id="e9daa-108">Se llama cuando un cliente está en el proceso de volver a conectar automáticamente una sesión con Escritorio remoto un servidor host de sesión de escritorio remoto (host de sesión de RD).</span><span class="sxs-lookup"><span data-stu-id="e9daa-108">Called when a client is in the process of automatically reconnecting a session with a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="e9daa-109">Se trata de una versión mejorada del método [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md) .</span><span class="sxs-lookup"><span data-stu-id="e9daa-109">This is an enhanced version of the [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9daa-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9daa-110">Syntax</span></span>


```C++
void OnAutoReconnecting2(
  [in] LONG         disconnectReason,
  [in] VARIANT_BOOL networkAvailable,
  [in] LONG         attemptCount,
  [in] LONG         maxAttemptCount
);
```



## <a name="parameters"></a><span data-ttu-id="e9daa-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9daa-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9daa-112">*disconnectReason* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e9daa-112">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9daa-113">Código que describe el motivo de la última desconexión de la sesión.</span><span class="sxs-lookup"><span data-stu-id="e9daa-113">Code that describes the reason for the last session disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="e9daa-114">*networkAvailable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e9daa-114">*networkAvailable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9daa-115">Especifica si la red está disponible.</span><span class="sxs-lookup"><span data-stu-id="e9daa-115">Specifies if the network is available.</span></span>

</dd> <dt>

<span data-ttu-id="e9daa-116">*attemptCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e9daa-116">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9daa-117">Número de intentos realizados en el proceso de reconexión automática actual.</span><span class="sxs-lookup"><span data-stu-id="e9daa-117">Number of attempts that have been made in the current automatic reconnection process.</span></span> <span data-ttu-id="e9daa-118">Este recuento se incrementa en uno por cada intento realizado.</span><span class="sxs-lookup"><span data-stu-id="e9daa-118">This count increases by one for each attempt made.</span></span>

</dd> <dt>

<span data-ttu-id="e9daa-119">*maxAttemptCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e9daa-119">*maxAttemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9daa-120">Número máximo de intentos que se realizarán en el proceso de reconexión automática actual.</span><span class="sxs-lookup"><span data-stu-id="e9daa-120">The maximum number of attempts that will be made in the current automatic reconnection process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9daa-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9daa-121">Return value</span></span>

<span data-ttu-id="e9daa-122">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e9daa-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9daa-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9daa-123">Requirements</span></span>



| <span data-ttu-id="e9daa-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9daa-124">Requirement</span></span> | <span data-ttu-id="e9daa-125">Value</span><span class="sxs-lookup"><span data-stu-id="e9daa-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9daa-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9daa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e9daa-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e9daa-127">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="e9daa-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9daa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e9daa-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9daa-129">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="e9daa-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e9daa-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="e9daa-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9daa-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e9daa-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e9daa-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9daa-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9daa-133"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9daa-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9daa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9daa-135">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="e9daa-135">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





