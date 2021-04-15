---
description: GUID de la partición del objeto de la clase de evento.
ms.assetid: 154849ac-350c-4b2f-bb51-ac6973f0a8fa
title: 'IEventSubscription3:: EventClassPartitionID (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.EventClassPartitionID
- IEventSubscription3.get_EventClassPartitionID
- IEventSubscription3.put_EventClassPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: d41d3e2a170deffb73f1f533226421d88f150c01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539304"
---
# <a name="ieventsubscription3eventclasspartitionid-property"></a><span data-ttu-id="44ff2-103">IEventSubscription3:: EventClassPartitionID (propiedad)</span><span class="sxs-lookup"><span data-stu-id="44ff2-103">IEventSubscription3::EventClassPartitionID property</span></span>

<span data-ttu-id="44ff2-104">GUID de la partición del objeto de la clase de evento.</span><span class="sxs-lookup"><span data-stu-id="44ff2-104">The partition GUID of the event class object.</span></span>

<span data-ttu-id="44ff2-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="44ff2-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="44ff2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44ff2-106">Syntax</span></span>


```C++
HRESULT put_EventClassPartitionID(
  [in]          BSTR bstrEventClassPartitionID
);

HRESULT get_EventClassPartitionID(
  [out, retval] BSTR *pbstrEventClassPartitionID
);
```



## <a name="property-value"></a><span data-ttu-id="44ff2-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="44ff2-107">Property value</span></span>

<span data-ttu-id="44ff2-108">Cadena que contiene el GUID de la partición de la clase de eventos.</span><span class="sxs-lookup"><span data-stu-id="44ff2-108">A string containing the GUID of the event class partition.</span></span>

## <a name="error-codes"></a><span data-ttu-id="44ff2-109">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="44ff2-109">Error codes</span></span>

<span data-ttu-id="44ff2-110">Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ FAIL y S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="44ff2-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="44ff2-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44ff2-111">Requirements</span></span>



| <span data-ttu-id="44ff2-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="44ff2-112">Requirement</span></span> | <span data-ttu-id="44ff2-113">Value</span><span class="sxs-lookup"><span data-stu-id="44ff2-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="44ff2-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44ff2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="44ff2-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="44ff2-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="44ff2-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44ff2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="44ff2-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="44ff2-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="44ff2-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="44ff2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44ff2-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="44ff2-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




