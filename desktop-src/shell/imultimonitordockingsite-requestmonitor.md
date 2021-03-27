---
description: Comprueba que el monitor está activo y disponible.
title: 'IMultiMonitorDockingSite:: RequestMonitor (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.RequestMonitor
api_type:
- COM
api_location: ''
ms.assetid: 9aa6eb20-de39-41f7-a17e-183f4088f972
ms.openlocfilehash: 5389b10af9aaa3da5d3106d82a4fbdcbd614a094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003159"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a><span data-ttu-id="9cae5-103">IMultiMonitorDockingSite:: RequestMonitor (método)</span><span class="sxs-lookup"><span data-stu-id="9cae5-103">IMultiMonitorDockingSite::RequestMonitor method</span></span>

<span data-ttu-id="9cae5-104">Comprueba que el monitor está activo y disponible.</span><span class="sxs-lookup"><span data-stu-id="9cae5-104">Verifies that the monitor is active and available.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cae5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9cae5-105">Syntax</span></span>


```C++
HRESULT RequestMonitor(
  [in] IUnknown *punkSrc,
  [in] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="9cae5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9cae5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cae5-107">*punkSrc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9cae5-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cae5-108">Tipo: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="9cae5-108">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="9cae5-109">Un puntero al objeto que implementa la interfaz [_ *IDockingWindow* \*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) .</span><span class="sxs-lookup"><span data-stu-id="9cae5-109">A pointer to the object implementing the [_ *IDockingWindow*\*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface.</span></span>

</dd> <dt>

<span data-ttu-id="9cae5-110">*phMon* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9cae5-110">*phMon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cae5-111">Tipo: \**HMONITOR \** _</span><span class="sxs-lookup"><span data-stu-id="9cae5-111">Type: \**HMONITOR\** _</span></span>

<span data-ttu-id="9cae5-112">Puntero al identificador del monitor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9cae5-112">A pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cae5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9cae5-113">Return value</span></span>

<span data-ttu-id="9cae5-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="9cae5-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="9cae5-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9cae5-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9cae5-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9cae5-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cae5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cae5-117">Requirements</span></span>



| <span data-ttu-id="9cae5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cae5-118">Requirement</span></span> | <span data-ttu-id="9cae5-119">Value</span><span class="sxs-lookup"><span data-stu-id="9cae5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="9cae5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cae5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9cae5-121">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9cae5-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9cae5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cae5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9cae5-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9cae5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
