---
description: Recupera el número de versión del sistema de eventos.
ms.assetid: 6355f1b3-e1e7-435f-9795-d92464e004ae
title: 'IEventSystem2:: GetVersion (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.GetVersion
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2c75538d9fd71cb8ee81e454249fd5116ccd090c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496655"
---
# <a name="ieventsystem2getversion-method"></a><span data-ttu-id="d89bf-103">IEventSystem2:: GetVersion (método)</span><span class="sxs-lookup"><span data-stu-id="d89bf-103">IEventSystem2::GetVersion method</span></span>

<span data-ttu-id="d89bf-104">Recupera el número de versión del sistema de eventos.</span><span class="sxs-lookup"><span data-stu-id="d89bf-104">Retrieves the version number of the event system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d89bf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d89bf-105">Syntax</span></span>


```C++
HRESULT GetVersion(
  [out] int *pnVersion
);
```



## <a name="parameters"></a><span data-ttu-id="d89bf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d89bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d89bf-107">*pnVersion* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d89bf-107">*pnVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d89bf-108">Número de versión del sistema de eventos.</span><span class="sxs-lookup"><span data-stu-id="d89bf-108">The version number of the event system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d89bf-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d89bf-109">Return value</span></span>

<span data-ttu-id="d89bf-110">Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ FAIL y S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d89bf-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="d89bf-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d89bf-111">Requirements</span></span>



| <span data-ttu-id="d89bf-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d89bf-112">Requirement</span></span> | <span data-ttu-id="d89bf-113">Value</span><span class="sxs-lookup"><span data-stu-id="d89bf-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d89bf-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d89bf-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d89bf-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d89bf-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d89bf-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d89bf-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d89bf-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d89bf-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d89bf-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="d89bf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d89bf-119">**IEventSystem2**</span><span class="sxs-lookup"><span data-stu-id="d89bf-119">**IEventSystem2**</span></span>](ieventsystem2.md)
</dt> </dl>

 

 




