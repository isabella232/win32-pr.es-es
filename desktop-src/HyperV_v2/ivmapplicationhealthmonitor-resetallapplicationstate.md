---
description: Restablece el estado de mantenimiento de todas las aplicaciones de una máquina virtual.
ms.assetid: DB0B2FB3-87EB-44B2-9C4E-849BCE594E89
title: 'IVmApplicationHealthMonitor:: ResetAllApplicationState (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.ResetAllApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: b13781d26c256e41ea6685b19a3097236ebbdb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908449"
---
# <a name="ivmapplicationhealthmonitorresetallapplicationstate-method"></a><span data-ttu-id="2abe0-103">IVmApplicationHealthMonitor:: ResetAllApplicationState (método)</span><span class="sxs-lookup"><span data-stu-id="2abe0-103">IVmApplicationHealthMonitor::ResetAllApplicationState method</span></span>

<span data-ttu-id="2abe0-104">Restablece el estado de mantenimiento de todas las aplicaciones de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2abe0-104">Resets the health state for all applications in a virtual machine.</span></span> <span data-ttu-id="2abe0-105">Si se realiza correctamente, el estado de mantenimiento de todas las aplicaciones supervisadas se establecerá en **ApplicationStateHealthy**.</span><span class="sxs-lookup"><span data-stu-id="2abe0-105">If successful, the health state for all monitored applications will be set to **ApplicationStateHealthy**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2abe0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2abe0-106">Syntax</span></span>


```C++
HRESULT ResetAllApplicationState();
```



## <a name="parameters"></a><span data-ttu-id="2abe0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2abe0-107">Parameters</span></span>

<span data-ttu-id="2abe0-108">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2abe0-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2abe0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2abe0-109">Return value</span></span>

<span data-ttu-id="2abe0-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2abe0-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2abe0-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2abe0-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2abe0-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2abe0-112">Remarks</span></span>

<span data-ttu-id="2abe0-113">Para usar este elemento de programación, los componentes de integración de Windows 8 deben estar instalados en la máquina virtual en la que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2abe0-113">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="2abe0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2abe0-114">Requirements</span></span>



| <span data-ttu-id="2abe0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abe0-115">Requirement</span></span> | <span data-ttu-id="2abe0-116">Value</span><span class="sxs-lookup"><span data-stu-id="2abe0-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abe0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2abe0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2abe0-118">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="2abe0-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="2abe0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2abe0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2abe0-120">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="2abe0-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2abe0-121">Versión</span><span class="sxs-lookup"><span data-stu-id="2abe0-121">Version</span></span><br/>                  | <span data-ttu-id="2abe0-122">Componentes de integración para Windows 8</span><span class="sxs-lookup"><span data-stu-id="2abe0-122">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="2abe0-123">IDL</span><span class="sxs-lookup"><span data-stu-id="2abe0-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2abe0-124"><dt>VmApplicationHealthMonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2abe0-124"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2abe0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2abe0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2abe0-126">**IVmApplicationHealthMonitor**</span><span class="sxs-lookup"><span data-stu-id="2abe0-126">**IVmApplicationHealthMonitor**</span></span>](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




