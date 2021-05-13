---
description: Cambios que se usan para las barras de herramientas acopladas en un sistema de varios monitores.
title: IMultiMonitorDockingSite::SetMonitor (Método)
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
ms.openlocfilehash: be773ee68c214f6a2fab8da89f1f48b867e71239
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841946"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a><span data-ttu-id="b2099-103">IMultiMonitorDockingSite::SetMonitor (Método)</span><span class="sxs-lookup"><span data-stu-id="b2099-103">IMultiMonitorDockingSite::SetMonitor method</span></span>

<span data-ttu-id="b2099-104">Cambios que se usan para las barras de herramientas acopladas en un sistema de varios monitores.</span><span class="sxs-lookup"><span data-stu-id="b2099-104">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2099-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2099-105">Syntax</span></span>


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a><span data-ttu-id="b2099-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2099-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2099-107">*yerbaSrc* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b2099-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2099-108">Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="b2099-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="b2099-109">Puntero al objeto que implementa la [**interfaz IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) para la que se modifica el monitor.</span><span class="sxs-lookup"><span data-stu-id="b2099-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being altered.</span></span>

</dd> <dt>

<span data-ttu-id="b2099-110">*hMonNew* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b2099-110">*hMonNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2099-111">Tipo: **HMONITOR**</span><span class="sxs-lookup"><span data-stu-id="b2099-111">Type: **HMONITOR**</span></span>

<span data-ttu-id="b2099-112">Identificador del monitor que reemplaza al monitor predeterminado existente.</span><span class="sxs-lookup"><span data-stu-id="b2099-112">A handle to the monitor that replaces the existing default monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b2099-113">*phMonOld* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b2099-113">*phMonOld* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2099-114">Tipo: **HMONITOR \***</span><span class="sxs-lookup"><span data-stu-id="b2099-114">Type: **HMONITOR\***</span></span>

<span data-ttu-id="b2099-115">Cuando esta función vuelve, contiene un puntero al identificador del monitor predeterminado anterior.</span><span class="sxs-lookup"><span data-stu-id="b2099-115">When this function returns, contains a pointer to the previous default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2099-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2099-116">Return value</span></span>

<span data-ttu-id="b2099-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b2099-117">Type: **HRESULT**</span></span>

<span data-ttu-id="b2099-118">Si este método se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b2099-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b2099-119">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="b2099-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2099-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2099-120">Requirements</span></span>



| <span data-ttu-id="b2099-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2099-121">Requirement</span></span> | <span data-ttu-id="b2099-122">Value</span><span class="sxs-lookup"><span data-stu-id="b2099-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="b2099-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2099-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b2099-124">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="b2099-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b2099-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2099-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b2099-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b2099-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
