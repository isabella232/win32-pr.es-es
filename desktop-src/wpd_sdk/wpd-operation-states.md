---
description: Los \_ valores de enumeración de Estados de la operación de WPD \_ describen el estado actual de una operación en curso.
ms.assetid: a002f735-e385-4c7c-b734-e70a9c6842ca
title: Enumeración WPD_OPERATION_STATES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_OPERATION_STATES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1746ab6a798c74974708ac10b9c4d137bf6c1d42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699964"
---
# <a name="wpd_operation_states-enumeration"></a><span data-ttu-id="93d7f-103">\_Enumeración de Estados de operación de WPD \_</span><span class="sxs-lookup"><span data-stu-id="93d7f-103">WPD\_OPERATION\_STATES enumeration</span></span>

<span data-ttu-id="93d7f-104">Los valores de enumeración de **\_ \_ Estados** de la operación de WPD describen el estado actual de una operación en curso.</span><span class="sxs-lookup"><span data-stu-id="93d7f-104">The **WPD\_OPERATION\_STATES** enumeration values describe the current state of an operation in progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="93d7f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93d7f-105">Syntax</span></span>


```C++
typedef enum tagWPD_OPERATION_STATES { 
  WPD_OPERATION_STATE_UNSPECIFIED  = 0,
  WPD_OPERATION_STATE_STARTED      = 1,
  WPD_OPERATION_STATE_RUNNING      = 2,
  WPD_OPERATION_STATE_PAUSED       = 3,
  WPD_OPERATION_STATE_CANCELLED    = 4,
  WPD_OPERATION_STATE_FINISHED     = 5,
  WPD_OPERATION_STATE_ABORTED      = 6
} WPD_OPERATION_STATES;
```



## <a name="constants"></a><span data-ttu-id="93d7f-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="93d7f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="93d7f-107"><span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**Estado de la operación de WPD no \_ \_ \_ especificado**</span><span class="sxs-lookup"><span data-stu-id="93d7f-107"><span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**WPD\_OPERATION\_STATE\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="93d7f-108">La operación actual está en un estado no especificado (no establecido) y se desconoce.</span><span class="sxs-lookup"><span data-stu-id="93d7f-108">The current operation is in an unspecified state (not set) and unknown.</span></span>

</dd> <dt>

<span data-ttu-id="93d7f-109"><span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**Estado de la operación de WPD \_ \_ \_ iniciado**</span><span class="sxs-lookup"><span data-stu-id="93d7f-109"><span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**WPD\_OPERATION\_STATE\_STARTED**</span></span>
</dt> <dd>

<span data-ttu-id="93d7f-110">La operación se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="93d7f-110">The operation is started.</span></span>

</dd> <dt>

<span data-ttu-id="93d7f-111"><span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**Estado de la operación de WPD en \_ \_ \_ ejecución**</span><span class="sxs-lookup"><span data-stu-id="93d7f-111"><span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**WPD\_OPERATION\_STATE\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="93d7f-112">La operación se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="93d7f-112">The operation is running.</span></span>

</dd> <dt>

<span data-ttu-id="93d7f-113"><span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**Estado de la operación de WPD en \_ \_ \_ pausa**</span><span class="sxs-lookup"><span data-stu-id="93d7f-113"><span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**WPD\_OPERATION\_STATE\_PAUSED**</span></span>
</dt> <dd>

<span data-ttu-id="93d7f-114">La operación está en pausa.</span><span class="sxs-lookup"><span data-stu-id="93d7f-114">The operation is paused.</span></span>

</dd> <dt>

<span data-ttu-id="93d7f-115"><span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**Estado de operación de WPD \_ \_ \_ cancelado**</span><span class="sxs-lookup"><span data-stu-id="93d7f-115"><span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**WPD\_OPERATION\_STATE\_CANCELLED**</span></span>
</dt> <dd>

<span data-ttu-id="93d7f-116">La operación se cancela.</span><span class="sxs-lookup"><span data-stu-id="93d7f-116">The operation is canceled.</span></span>

</dd> <dt>

<span data-ttu-id="93d7f-117"><span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**Estado de la operación de WPD \_ \_ \_ finalizado**</span><span class="sxs-lookup"><span data-stu-id="93d7f-117"><span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**WPD\_OPERATION\_STATE\_FINISHED**</span></span>
</dt> <dd>

<span data-ttu-id="93d7f-118">La operación ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="93d7f-118">The operation is finished.</span></span>

</dd> <dt>

<span data-ttu-id="93d7f-119"><span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**Estado de operación de WPD \_ \_ \_ anulado**</span><span class="sxs-lookup"><span data-stu-id="93d7f-119"><span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**WPD\_OPERATION\_STATE\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="93d7f-120">La operación se ha anulado.</span><span class="sxs-lookup"><span data-stu-id="93d7f-120">The operation is aborted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93d7f-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93d7f-121">Remarks</span></span>

<span data-ttu-id="93d7f-122">Estos valores se reciben en la devolución de llamada definida por la aplicación ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).</span><span class="sxs-lookup"><span data-stu-id="93d7f-122">These values are received in the application-defined callback ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).</span></span>

## <a name="requirements"></a><span data-ttu-id="93d7f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93d7f-123">Requirements</span></span>



| <span data-ttu-id="93d7f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="93d7f-124">Requirement</span></span> | <span data-ttu-id="93d7f-125">Value</span><span class="sxs-lookup"><span data-stu-id="93d7f-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="93d7f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93d7f-126">Header</span></span><br/> | <dl> <span data-ttu-id="93d7f-127"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="93d7f-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93d7f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="93d7f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93d7f-129">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="93d7f-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




