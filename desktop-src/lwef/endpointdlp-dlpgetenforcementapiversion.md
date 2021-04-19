---
description: Recupera la versión de la API de prevención de pérdida de datos (DLP) del punto de conexión en el dispositivo actual.
title: Función DlpGetEnforcementApiVersion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpGetEnforcementApiVersion
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d2b38b6bdcfd761b8ae3c90ee5d3b430767ad29c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495949"
---
# <a name="dlpgetenforcementapiversion-function"></a><span data-ttu-id="b6df9-103">Función DlpGetEnforcementApiVersion</span><span class="sxs-lookup"><span data-stu-id="b6df9-103">DlpGetEnforcementApiVersion function</span></span>

<span data-ttu-id="b6df9-104">Recupera la versión de la API de prevención de pérdida de datos (DLP) del punto de conexión en el dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="b6df9-104">Retrieves the version of the endpoint Data Loss Prevention (DLP) API on the current device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6df9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6df9-105">Syntax</span></span>


```C++
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);
```



## <a name="parameters"></a><span data-ttu-id="b6df9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6df9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6df9-107">*MajorVersion* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b6df9-107">*MajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6df9-108">DWORD **que** especifica el número de versión principal.</span><span class="sxs-lookup"><span data-stu-id="b6df9-108">A **DWORD** specifying the major version number.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="b6df9-109">*MajorVersion* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b6df9-109">*MajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6df9-110">DWORD **que** especifica el número de versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="b6df9-110">A **DWORD** specifying the minor version number.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="b6df9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6df9-111">Return value</span></span>

<span data-ttu-id="b6df9-112">Devuelve un valor HRESULT que incluye, entre otros, los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b6df9-112">Returns an HRESULT including, but not limited to, the following values.</span></span>

| <span data-ttu-id="b6df9-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b6df9-113">HRESULT</span></span> | <span data-ttu-id="b6df9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6df9-114">Description</span></span> |
|---------|-------------|
| <span data-ttu-id="b6df9-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="b6df9-115">S_OK</span></span> | <span data-ttu-id="b6df9-116">La función se completó correctamente</span><span class="sxs-lookup"><span data-stu-id="b6df9-116">The function completed successfully</span></span> |




## <a name="remarks"></a><span data-ttu-id="b6df9-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6df9-117">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="b6df9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6df9-118">Requirements</span></span>



| <span data-ttu-id="b6df9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6df9-119">Requirement</span></span>          |    <span data-ttu-id="b6df9-120">Value</span><span class="sxs-lookup"><span data-stu-id="b6df9-120">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6df9-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6df9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b6df9-122">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="b6df9-122">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="b6df9-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b6df9-123">DLL</span></span><br/>                      | <span data-ttu-id="b6df9-124">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="b6df9-124">EndpointDlp.dll</span></span> |