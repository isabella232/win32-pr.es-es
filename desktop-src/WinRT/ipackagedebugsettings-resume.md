---
description: Reanuda los procesos del paquete si están suspendidos.
ms.assetid: c5376e00-b4b7-4a81-a84c-3a46758fe130
title: 'IPackageDebugSettings:: resume (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Resume
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 2d36b11baffdc3f587924acd1732cbdfdb43d37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715152"
---
# <a name="ipackagedebugsettingsresume-method"></a><span data-ttu-id="720c8-103">IPackageDebugSettings:: resume (método)</span><span class="sxs-lookup"><span data-stu-id="720c8-103">IPackageDebugSettings::Resume method</span></span>

<span data-ttu-id="720c8-104">Reanuda los procesos del paquete si están suspendidos.</span><span class="sxs-lookup"><span data-stu-id="720c8-104">Resumes the processes of the package if they are currently suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="720c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="720c8-105">Syntax</span></span>


```C++
HRESULT Resume(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a><span data-ttu-id="720c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="720c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="720c8-107">*packageFullName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="720c8-107">*packageFullName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="720c8-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="720c8-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="720c8-109">Nombre completo del paquete.</span><span class="sxs-lookup"><span data-stu-id="720c8-109">The package full name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="720c8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="720c8-110">Return value</span></span>

<span data-ttu-id="720c8-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="720c8-111">Type: **HRESULT**</span></span>

<span data-ttu-id="720c8-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="720c8-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="720c8-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="720c8-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="720c8-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="720c8-114">Remarks</span></span>

<span data-ttu-id="720c8-115">Cada proceso recibe el evento [**RESUMING**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="720c8-115">Each process receives the [**Resuming**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) event.</span></span> <span data-ttu-id="720c8-116">Puede ser útil para los desarrolladores recorrer el modo en que sus aplicaciones responden a este evento.</span><span class="sxs-lookup"><span data-stu-id="720c8-116">It can be useful for developers to step through how their apps respond to this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="720c8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="720c8-117">Requirements</span></span>



| <span data-ttu-id="720c8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="720c8-118">Requirement</span></span> | <span data-ttu-id="720c8-119">Value</span><span class="sxs-lookup"><span data-stu-id="720c8-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="720c8-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="720c8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="720c8-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="720c8-121">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="720c8-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="720c8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="720c8-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="720c8-123">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="720c8-124">IDL</span><span class="sxs-lookup"><span data-stu-id="720c8-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="720c8-125"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="720c8-125"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="720c8-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="720c8-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="720c8-127">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="720c8-127">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span></span>
</dt> </dl>

 

 
