---
description: Cambia el monitor que se usa para las barras de herramientas acopladas en un sistema de varios monitores.
title: 'IMultiMonitorDockingSite:: SetMonitor (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.SetMonitor
api_type:
- COM
api_location: ''
ms.assetid: ba4ace13-7096-4f05-bcb0-ab37f1632406
ms.openlocfilehash: cc177316a850bbf5059cabf48362ab8d5cbe2466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997968"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a><span data-ttu-id="d0d9f-103">IMultiMonitorDockingSite:: SetMonitor (método)</span><span class="sxs-lookup"><span data-stu-id="d0d9f-103">IMultiMonitorDockingSite::SetMonitor method</span></span>

<span data-ttu-id="d0d9f-104">Cambia el monitor que se usa para las barras de herramientas acopladas en un sistema de varios monitores.</span><span class="sxs-lookup"><span data-stu-id="d0d9f-104">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0d9f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0d9f-105">Syntax</span></span>


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a><span data-ttu-id="d0d9f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0d9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0d9f-107">*punkSrc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0d9f-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0d9f-108">Tipo: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="d0d9f-108">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="d0d9f-109">Puntero al objeto que implementa la interfaz [_ *IDockingWindow* \*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) para la que se está modificando el monitor.</span><span class="sxs-lookup"><span data-stu-id="d0d9f-109">A pointer to the object implementing the [_ *IDockingWindow*\*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being altered.</span></span>

</dd> <dt>

<span data-ttu-id="d0d9f-110">*hMonNew* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0d9f-110">*hMonNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0d9f-111">Tipo: **HMONITOR**</span><span class="sxs-lookup"><span data-stu-id="d0d9f-111">Type: **HMONITOR**</span></span>

<span data-ttu-id="d0d9f-112">Identificador del monitor que reemplaza el monitor predeterminado existente.</span><span class="sxs-lookup"><span data-stu-id="d0d9f-112">A handle to the monitor that replaces the existing default monitor.</span></span>

</dd> <dt>

<span data-ttu-id="d0d9f-113">*phMonOld* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d0d9f-113">*phMonOld* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0d9f-114">Tipo: \**HMONITOR \** _</span><span class="sxs-lookup"><span data-stu-id="d0d9f-114">Type: \**HMONITOR\** _</span></span>

<span data-ttu-id="d0d9f-115">Cuando esta función devuelve un valor, contiene un puntero al identificador del monitor predeterminado anterior.</span><span class="sxs-lookup"><span data-stu-id="d0d9f-115">When this function returns, contains a pointer to the previous default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0d9f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0d9f-116">Return value</span></span>

<span data-ttu-id="d0d9f-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d0d9f-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d0d9f-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d0d9f-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d0d9f-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d0d9f-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0d9f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0d9f-120">Requirements</span></span>



| <span data-ttu-id="d0d9f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0d9f-121">Requirement</span></span> | <span data-ttu-id="d0d9f-122">Value</span><span class="sxs-lookup"><span data-stu-id="d0d9f-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="d0d9f-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0d9f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d0d9f-124">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d0d9f-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d0d9f-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0d9f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d0d9f-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0d9f-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
