---
description: Obtiene el monitor predeterminado actual.
title: IMultiMonitorDockingSite::GetMonitor (método)
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
ms.openlocfilehash: 2cd437fd6c0e842eb314db6c57420af6b54b05ff
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840646"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a><span data-ttu-id="ee2f9-103">IMultiMonitorDockingSite::GetMonitor (método)</span><span class="sxs-lookup"><span data-stu-id="ee2f9-103">IMultiMonitorDockingSite::GetMonitor method</span></span>

<span data-ttu-id="ee2f9-104">Obtiene el monitor predeterminado actual.</span><span class="sxs-lookup"><span data-stu-id="ee2f9-104">Gets the current default monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee2f9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee2f9-105">Syntax</span></span>


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="ee2f9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee2f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee2f9-107">*yerbaSrc* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ee2f9-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee2f9-108">Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="ee2f9-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="ee2f9-109">Puntero al objeto que implementa la [**interfaz IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) para la que se solicita el monitor.</span><span class="sxs-lookup"><span data-stu-id="ee2f9-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="ee2f9-110">*phMon* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ee2f9-110">*phMon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee2f9-111">Tipo: **HMONITOR \***</span><span class="sxs-lookup"><span data-stu-id="ee2f9-111">Type: **HMONITOR\***</span></span>

<span data-ttu-id="ee2f9-112">Cuando la función devuelve un resultado, contiene un puntero al identificador del monitor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ee2f9-112">When the function returns, contains a pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee2f9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee2f9-113">Return value</span></span>

<span data-ttu-id="ee2f9-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ee2f9-114">Type: **HRESULT**</span></span>

<span data-ttu-id="ee2f9-115">Si este método se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ee2f9-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ee2f9-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="ee2f9-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee2f9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee2f9-117">Requirements</span></span>



| <span data-ttu-id="ee2f9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee2f9-118">Requirement</span></span> | <span data-ttu-id="ee2f9-119">Value</span><span class="sxs-lookup"><span data-stu-id="ee2f9-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="ee2f9-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee2f9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ee2f9-121">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="ee2f9-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ee2f9-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee2f9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ee2f9-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ee2f9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
