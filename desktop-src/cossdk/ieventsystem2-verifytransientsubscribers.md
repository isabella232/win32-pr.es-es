---
description: Comprueba la existencia de todos los suscriptores transitorios en el almacén de datos. Al llamar a este método, puede asegurarse de que todos los suscriptores transitorios enumerados en el almacén de datos estén activos.
ms.assetid: fffdde33-e960-42ef-a089-8ea8a6f33d52
title: 'IEventSystem2:: VerifyTransientSubscribers (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.VerifyTransientSubscribers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4415f405b95f341b645ca1dccbf254df2ffc7167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998244"
---
# <a name="ieventsystem2verifytransientsubscribers-method"></a><span data-ttu-id="553ab-104">IEventSystem2:: VerifyTransientSubscribers (método)</span><span class="sxs-lookup"><span data-stu-id="553ab-104">IEventSystem2::VerifyTransientSubscribers method</span></span>

<span data-ttu-id="553ab-105">Comprueba la existencia de todos los suscriptores transitorios en el almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="553ab-105">Verifies the existence of all transient subscribers in the data store.</span></span> <span data-ttu-id="553ab-106">Al llamar a este método, puede asegurarse de que todos los suscriptores transitorios enumerados en el almacén de datos estén activos.</span><span class="sxs-lookup"><span data-stu-id="553ab-106">By calling this method, you can ensure that all transient subscribers listed in the data store are active.</span></span>

## <a name="syntax"></a><span data-ttu-id="553ab-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="553ab-107">Syntax</span></span>


```C++
HRESULT VerifyTransientSubscribers();
```



## <a name="parameters"></a><span data-ttu-id="553ab-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="553ab-108">Parameters</span></span>

<span data-ttu-id="553ab-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="553ab-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="553ab-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="553ab-110">Return value</span></span>

<span data-ttu-id="553ab-111">Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ FAIL y S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="553ab-111">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="553ab-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="553ab-112">Requirements</span></span>



| <span data-ttu-id="553ab-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="553ab-113">Requirement</span></span> | <span data-ttu-id="553ab-114">Value</span><span class="sxs-lookup"><span data-stu-id="553ab-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="553ab-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="553ab-115">Minimum supported client</span></span><br/> | <span data-ttu-id="553ab-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="553ab-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="553ab-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="553ab-117">Minimum supported server</span></span><br/> | <span data-ttu-id="553ab-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="553ab-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="553ab-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="553ab-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="553ab-120">**IEventSystem2**</span><span class="sxs-lookup"><span data-stu-id="553ab-120">**IEventSystem2**</span></span>](ieventsystem2.md)
</dt> </dl>

 

 




