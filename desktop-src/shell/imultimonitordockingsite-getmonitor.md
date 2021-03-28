---
description: Obtiene el monitor predeterminado actual.
title: 'IMultiMonitorDockingSite:: GetMonitor (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.GetMonitor
api_type:
- COM
api_location: ''
ms.assetid: 0bae75eb-ebd5-4de4-9249-0e9bb489f61f
ms.openlocfilehash: 1260da5ee4404a7ec4597a57e7e3836d6f133426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997840"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a><span data-ttu-id="d75bd-103">IMultiMonitorDockingSite:: GetMonitor (método)</span><span class="sxs-lookup"><span data-stu-id="d75bd-103">IMultiMonitorDockingSite::GetMonitor method</span></span>

<span data-ttu-id="d75bd-104">Obtiene el monitor predeterminado actual.</span><span class="sxs-lookup"><span data-stu-id="d75bd-104">Gets the current default monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="d75bd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d75bd-105">Syntax</span></span>


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="d75bd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d75bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d75bd-107">*punkSrc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d75bd-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d75bd-108">Tipo: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="d75bd-108">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="d75bd-109">Puntero al objeto que implementa la interfaz [_ *IDockingWindow* \*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) para la que se solicita el monitor.</span><span class="sxs-lookup"><span data-stu-id="d75bd-109">A pointer to the object implementing the [_ *IDockingWindow*\*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="d75bd-110">*phMon* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d75bd-110">*phMon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d75bd-111">Tipo: \**HMONITOR \** _</span><span class="sxs-lookup"><span data-stu-id="d75bd-111">Type: \**HMONITOR\** _</span></span>

<span data-ttu-id="d75bd-112">Cuando la función devuelve un valor, contiene un puntero al identificador del monitor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d75bd-112">When the function returns, contains a pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d75bd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d75bd-113">Return value</span></span>

<span data-ttu-id="d75bd-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d75bd-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d75bd-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d75bd-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d75bd-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d75bd-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d75bd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d75bd-117">Requirements</span></span>



| <span data-ttu-id="d75bd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d75bd-118">Requirement</span></span> | <span data-ttu-id="d75bd-119">Value</span><span class="sxs-lookup"><span data-stu-id="d75bd-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="d75bd-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d75bd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d75bd-121">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d75bd-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d75bd-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d75bd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d75bd-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d75bd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
