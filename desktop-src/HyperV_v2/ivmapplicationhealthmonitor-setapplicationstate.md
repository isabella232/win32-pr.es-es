---
description: Establece el estado de mantenimiento de una aplicación que se ejecuta en una máquina virtual.
ms.assetid: 012190CA-9CBF-47B6-9C5D-F75D73B0499B
title: 'IVmApplicationHealthMonitor:: SetApplicationState (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.SetApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 8e6c64ecec827f6f75f382fbca7aadf8fc0c7dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687195"
---
# <a name="ivmapplicationhealthmonitorsetapplicationstate-method"></a><span data-ttu-id="78a27-103">IVmApplicationHealthMonitor:: SetApplicationState (método)</span><span class="sxs-lookup"><span data-stu-id="78a27-103">IVmApplicationHealthMonitor::SetApplicationState method</span></span>

<span data-ttu-id="78a27-104">Establece el estado de mantenimiento de una aplicación que se ejecuta en una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="78a27-104">Sets the health state of an application that is running in a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="78a27-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78a27-105">Syntax</span></span>


```C++
HRESULT SetApplicationState(
  [in] BSTR              Id,
  [in] BSTR              Name,
  [in] APPLICATION_STATE State
);
```



## <a name="parameters"></a><span data-ttu-id="78a27-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78a27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78a27-107">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="78a27-107">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78a27-108">Representación **BSTR** del **GUID** que identifica la aplicación.</span><span class="sxs-lookup"><span data-stu-id="78a27-108">A **BSTR** representation of the **GUID** that identifies the application.</span></span> <span data-ttu-id="78a27-109">Es responsabilidad de la aplicación que llama a crear y mantener los identificadores que usa para las aplicaciones que se están supervisando.</span><span class="sxs-lookup"><span data-stu-id="78a27-109">It is the calling application's responsibility to create and maintain the identifiers it uses for the applications being monitored.</span></span>

</dd> <dt>

<span data-ttu-id="78a27-110">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="78a27-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78a27-111">Nombre para mostrar de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="78a27-111">The display name of the application.</span></span> <span data-ttu-id="78a27-112">Este nombre se usa en una entrada del registro de eventos informativos para el cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="78a27-112">This name is used in an informational event log entry for the state change.</span></span>

</dd> <dt>

<span data-ttu-id="78a27-113">*Estado* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="78a27-113">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78a27-114">Un valor de la enumeración del [**\_ Estado**](application-state.md) de la aplicación que especifica el nuevo estado de mantenimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="78a27-114">A value of the [**APPLICATION\_STATE**](application-state.md) enumeration that specifies the new health state of the application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78a27-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78a27-115">Return value</span></span>

<span data-ttu-id="78a27-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="78a27-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="78a27-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="78a27-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="78a27-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78a27-118">Remarks</span></span>

<span data-ttu-id="78a27-119">El estado de las aplicaciones que se ejecutan en la máquina virtual se refleja en el \[ valor de la propiedad OperationalStatus 1 \] de la clase [**MSVM \_ HeartbeatComponent**](msvm-heartbeatcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="78a27-119">The state of the applications running in the virtual machine are reflected in the **OperationalStatus**\[1\] property value of the [**Msvm\_HeartbeatComponent**](msvm-heartbeatcomponent.md) class.</span></span>

<span data-ttu-id="78a27-120">Para usar este elemento de programación, los componentes de integración de Windows 8 deben estar instalados en la máquina virtual en la que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="78a27-120">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="78a27-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78a27-121">Requirements</span></span>



| <span data-ttu-id="78a27-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="78a27-122">Requirement</span></span> | <span data-ttu-id="78a27-123">Value</span><span class="sxs-lookup"><span data-stu-id="78a27-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78a27-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78a27-124">Minimum supported client</span></span><br/> | <span data-ttu-id="78a27-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="78a27-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="78a27-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78a27-126">Minimum supported server</span></span><br/> | <span data-ttu-id="78a27-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="78a27-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="78a27-128">Versión</span><span class="sxs-lookup"><span data-stu-id="78a27-128">Version</span></span><br/>                  | <span data-ttu-id="78a27-129">Componentes de integración para Windows 8</span><span class="sxs-lookup"><span data-stu-id="78a27-129">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="78a27-130">IDL</span><span class="sxs-lookup"><span data-stu-id="78a27-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="78a27-131"><dt>VmApplicationHealthMonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="78a27-131"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78a27-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="78a27-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78a27-133">**IVmApplicationHealthMonitor**</span><span class="sxs-lookup"><span data-stu-id="78a27-133">**IVmApplicationHealthMonitor**</span></span>](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




