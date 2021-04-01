---
title: MsimtfIsWindowFiltered función)
description: La función MsimtfIsWindowFiltered comprueba si AIMM (Administrador de métodos de entrada activos) filtra la ventana especificada.
ms.assetid: 1f5e98f1-3626-4aa5-b2da-b6bc48d02184
keywords:
- MsimtfIsWindowFiltered función de servicios de texto
topic_type:
- apiref
api_name:
- MsimtfIsWindowFiltered
api_location:
- msimtf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ad9bd9fb61c546ec3e2f1d96d5fc9cf932613a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150858"
---
# <a name="msimtfiswindowfiltered-function"></a><span data-ttu-id="88e42-104">MsimtfIsWindowFiltered función)</span><span class="sxs-lookup"><span data-stu-id="88e42-104">MsimtfIsWindowFiltered function</span></span>

<span data-ttu-id="88e42-105">La función **MsimtfIsWindowFiltered** comprueba si AIMM (Administrador de métodos de entrada activos) filtra la ventana especificada.</span><span class="sxs-lookup"><span data-stu-id="88e42-105">The **MsimtfIsWindowFiltered** function tests if the given window is filtered by AIMM (Active Input Method Manager).</span></span>

## <a name="syntax"></a><span data-ttu-id="88e42-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88e42-106">Syntax</span></span>


```C++
BOOL CALLBACK MsimtfIsWindowFiltered(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="88e42-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88e42-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88e42-108">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="88e42-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88e42-109">Identificador de ventana que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="88e42-109">A window handle to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88e42-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88e42-110">Return value</span></span>



| <span data-ttu-id="88e42-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="88e42-111">Return code</span></span>                                                                          | <span data-ttu-id="88e42-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="88e42-112">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="88e42-113"><dt>**REALES**</dt></span><span class="sxs-lookup"><span data-stu-id="88e42-113"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="88e42-114">Si esta ventana está filtrada por el administrador de métodos de entrada activo.</span><span class="sxs-lookup"><span data-stu-id="88e42-114">If this window is filtered by Active Input Method Manager.</span></span><br/>     |
| <dl> <span data-ttu-id="88e42-115"><dt>**ES**</dt></span><span class="sxs-lookup"><span data-stu-id="88e42-115"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="88e42-116">Si esta ventana no está filtrada por el administrador de métodos de entrada activo.</span><span class="sxs-lookup"><span data-stu-id="88e42-116">If this window is not filtered by Active Input Method Manager.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="88e42-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88e42-117">Remarks</span></span>

<span data-ttu-id="88e42-118">Una ventana se puede filtrar por IActiveIMMApp:: FilterClientWindows.</span><span class="sxs-lookup"><span data-stu-id="88e42-118">A window can be filtered by IActiveIMMApp::FilterClientWindows.</span></span>

## <a name="requirements"></a><span data-ttu-id="88e42-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88e42-119">Requirements</span></span>



| <span data-ttu-id="88e42-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="88e42-120">Requirement</span></span> | <span data-ttu-id="88e42-121">Value</span><span class="sxs-lookup"><span data-stu-id="88e42-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88e42-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88e42-122">Minimum supported client</span></span><br/> | <span data-ttu-id="88e42-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="88e42-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="88e42-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88e42-124">Minimum supported server</span></span><br/> | <span data-ttu-id="88e42-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="88e42-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="88e42-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="88e42-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88e42-127"><dt>Msimtf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88e42-127"><dt>Msimtf.dll</dt></span></span> </dl> |



 

 





