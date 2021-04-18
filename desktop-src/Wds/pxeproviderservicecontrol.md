---
title: Función de devolución de llamada PxeProviderServiceControl
description: Se llama cuando el servicio WDS recibe un código de control de servicio.
ms.assetid: 180ddcda-d111-4c81-9177-db99cbf1449f
keywords:
- Función de devolución de llamada PxeProviderServiceControl servicios de implementación de Windows
topic_type:
- apiref
api_name:
- PxeProviderServiceControl
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c8a2c71b7b386254622758efa5f3dc5269a131d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705140"
---
# <a name="pxeproviderservicecontrol-callback-function"></a><span data-ttu-id="186fd-104">Función de devolución de llamada PxeProviderServiceControl</span><span class="sxs-lookup"><span data-stu-id="186fd-104">PxeProviderServiceControl callback function</span></span>

<span data-ttu-id="186fd-105">Se llama cuando el servicio WDS recibe un código de control de servicio.</span><span class="sxs-lookup"><span data-stu-id="186fd-105">Called when a service control code is received by the WDS service.</span></span> <span data-ttu-id="186fd-106">Esta función de devolución de llamada se registra mediante una llamada a la función [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) con el parámetro *CallbackType* establecido en el **control de servicio de devolución de \_ llamada \_ \_ PXE**.</span><span class="sxs-lookup"><span data-stu-id="186fd-106">This callback function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_SERVICE\_CONTROL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="186fd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="186fd-107">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderServiceControl(
  _In_ PVOID pContext,
       DWORD dwControl
);
```



## <a name="parameters"></a><span data-ttu-id="186fd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="186fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="186fd-109">*pContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="186fd-109">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="186fd-110">Valor de contexto que se pasa a la función [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="186fd-110">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> <dt>

<span data-ttu-id="186fd-111">*dwControl*</span><span class="sxs-lookup"><span data-stu-id="186fd-111">*dwControl*</span></span> 
</dt> <dd>

<span data-ttu-id="186fd-112">Código de control.</span><span class="sxs-lookup"><span data-stu-id="186fd-112">Control code.</span></span> <span data-ttu-id="186fd-113">Para obtener la lista de valores posibles, vea el parámetro *dwControl* de la función [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) .</span><span class="sxs-lookup"><span data-stu-id="186fd-113">For the list of possible values, see the *dwControl* parameter of the [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="186fd-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="186fd-114">Return value</span></span>

<span data-ttu-id="186fd-115">Si el cierre del proveedor se realiza correctamente, la devolución de llamada debe devolver el **error \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="186fd-115">If the provider shutdown succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="186fd-116">En caso de error, se debe devolver un código de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="186fd-116">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="186fd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="186fd-117">Requirements</span></span>



| <span data-ttu-id="186fd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="186fd-118">Requirement</span></span> | <span data-ttu-id="186fd-119">Value</span><span class="sxs-lookup"><span data-stu-id="186fd-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="186fd-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="186fd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="186fd-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="186fd-121">None supported</span></span><br/>                                                          |
| <span data-ttu-id="186fd-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="186fd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="186fd-123">Windows Server 2008, Windows Server 2003 con \[ solo aplicaciones de escritorio de SP2\]</span><span class="sxs-lookup"><span data-stu-id="186fd-123">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="186fd-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="186fd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="186fd-125">Funciones de servidor de servicios de implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="186fd-125">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="186fd-126">**PxeRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="186fd-126">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

