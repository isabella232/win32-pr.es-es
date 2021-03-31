---
description: Suspende los procesos del paquete si se están ejecutando actualmente.
ms.assetid: 83f44285-46ed-4968-b0af-7964dfacf602
title: 'IPackageDebugSettings:: Suspend (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Suspend
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 385ddc856661090caec4345df6651605b67fe883
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809770"
---
# <a name="ipackagedebugsettingssuspend-method"></a><span data-ttu-id="d20f2-103">IPackageDebugSettings:: Suspend (método)</span><span class="sxs-lookup"><span data-stu-id="d20f2-103">IPackageDebugSettings::Suspend method</span></span>

<span data-ttu-id="d20f2-104">Suspende los procesos del paquete si se están ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="d20f2-104">Suspends the processes of the package if they are currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="d20f2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d20f2-105">Syntax</span></span>


```C++
HRESULT Suspend(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a><span data-ttu-id="d20f2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d20f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d20f2-107">*packageFullName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d20f2-107">*packageFullName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d20f2-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="d20f2-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="d20f2-109">Nombre completo del paquete.</span><span class="sxs-lookup"><span data-stu-id="d20f2-109">The package full name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d20f2-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d20f2-110">Return value</span></span>

<span data-ttu-id="d20f2-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d20f2-111">Type: **HRESULT**</span></span>

<span data-ttu-id="d20f2-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="d20f2-112">This method can return one of these values.</span></span>



| <span data-ttu-id="d20f2-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d20f2-113">Return code</span></span>                                                                                            | <span data-ttu-id="d20f2-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d20f2-114">Description</span></span>                                      |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="d20f2-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d20f2-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="d20f2-116">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d20f2-116">The operation succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="d20f2-117"><dt>**E \_ STATECHANGE no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d20f2-117"><dt>**E\_ILLEGAL\_STATECHANGE**</dt></span></span> </dl> | <span data-ttu-id="d20f2-118">El proceso no se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="d20f2-118">The process is not currently running.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d20f2-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d20f2-119">Remarks</span></span>

<span data-ttu-id="d20f2-120">Cada proceso recibe el evento de [**suspensión**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="d20f2-120">Each process receives the [**Suspending**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) event.</span></span> <span data-ttu-id="d20f2-121">Puede ser útil para los desarrolladores recorrer el modo en que sus aplicaciones responden a este evento.</span><span class="sxs-lookup"><span data-stu-id="d20f2-121">It can be useful for developers to step through how their apps respond to this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="d20f2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d20f2-122">Requirements</span></span>



| <span data-ttu-id="d20f2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d20f2-123">Requirement</span></span> | <span data-ttu-id="d20f2-124">Value</span><span class="sxs-lookup"><span data-stu-id="d20f2-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d20f2-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d20f2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d20f2-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d20f2-126">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="d20f2-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d20f2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d20f2-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d20f2-128">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="d20f2-129">IDL</span><span class="sxs-lookup"><span data-stu-id="d20f2-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d20f2-130"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d20f2-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d20f2-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="d20f2-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="d20f2-132">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d20f2-132">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span></span>
</dt> </dl>

 

 
