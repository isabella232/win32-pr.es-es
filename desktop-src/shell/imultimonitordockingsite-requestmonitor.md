---
description: Comprueba que el monitor está activo y disponible.
title: IMultiMonitorDockingSite::RequestMonitor (Método)
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
ms.openlocfilehash: 7f219e5fd62fb4f85fd206501e6a53ac3927195a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841976"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a><span data-ttu-id="1d3af-103">IMultiMonitorDockingSite::RequestMonitor (Método)</span><span class="sxs-lookup"><span data-stu-id="1d3af-103">IMultiMonitorDockingSite::RequestMonitor method</span></span>

<span data-ttu-id="1d3af-104">Comprueba que el monitor está activo y disponible.</span><span class="sxs-lookup"><span data-stu-id="1d3af-104">Verifies that the monitor is active and available.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d3af-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d3af-105">Syntax</span></span>


```C++
HRESULT RequestMonitor(
  [in] IUnknown *punkSrc,
  [in] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="1d3af-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d3af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d3af-107">*yerbaSrc* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1d3af-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d3af-108">Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="1d3af-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="1d3af-109">Puntero al objeto que implementa la [**interfaz IDockingWindow.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow)</span><span class="sxs-lookup"><span data-stu-id="1d3af-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface.</span></span>

</dd> <dt>

<span data-ttu-id="1d3af-110">*phMon* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1d3af-110">*phMon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d3af-111">Tipo: **HMONITOR \***</span><span class="sxs-lookup"><span data-stu-id="1d3af-111">Type: **HMONITOR\***</span></span>

<span data-ttu-id="1d3af-112">Puntero al identificador del monitor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1d3af-112">A pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d3af-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d3af-113">Return value</span></span>

<span data-ttu-id="1d3af-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1d3af-114">Type: **HRESULT**</span></span>

<span data-ttu-id="1d3af-115">Si este método se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1d3af-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1d3af-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="1d3af-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d3af-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d3af-117">Requirements</span></span>



| <span data-ttu-id="1d3af-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d3af-118">Requirement</span></span> | <span data-ttu-id="1d3af-119">Value</span><span class="sxs-lookup"><span data-stu-id="1d3af-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="1d3af-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d3af-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1d3af-121">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="1d3af-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1d3af-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d3af-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1d3af-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d3af-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
