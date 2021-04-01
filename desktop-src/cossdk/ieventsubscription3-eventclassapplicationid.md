---
description: GUID de la aplicación del objeto de la clase de evento.
ms.assetid: 0d19183a-429c-4564-b6a5-f06481d27e00
title: 'IEventSubscription3:: EventClassApplicationID (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.EventClassApplicationID
- IEventSubscription3.get_EventClassApplicationID
- IEventSubscription3.put_EventClassApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3e80a8d8f557c80a1b2605328728260eb8ae7bd7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153202"
---
# <a name="ieventsubscription3eventclassapplicationid-property"></a><span data-ttu-id="a3ab6-103">IEventSubscription3:: EventClassApplicationID (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a3ab6-103">IEventSubscription3::EventClassApplicationID property</span></span>

<span data-ttu-id="a3ab6-104">GUID de la aplicación del objeto de la clase de evento.</span><span class="sxs-lookup"><span data-stu-id="a3ab6-104">The application GUID of the event class object.</span></span>

<span data-ttu-id="a3ab6-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a3ab6-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3ab6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3ab6-106">Syntax</span></span>


```C++
HRESULT put_EventClassApplicationID(
  [in]          BSTR bstrEventClassApplicationID
);

HRESULT get_EventClassApplicationID(
  [out, retval] BSTR *pbstrEventClassApplicationID
);
```



## <a name="property-value"></a><span data-ttu-id="a3ab6-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a3ab6-107">Property value</span></span>

<span data-ttu-id="a3ab6-108">Cadena que contiene el GUID de la aplicación de la clase de eventos.</span><span class="sxs-lookup"><span data-stu-id="a3ab6-108">A string containing the GUID of the event class application.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a3ab6-109">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a3ab6-109">Error codes</span></span>

<span data-ttu-id="a3ab6-110">Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ FAIL y S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a3ab6-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3ab6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3ab6-111">Requirements</span></span>



| <span data-ttu-id="a3ab6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3ab6-112">Requirement</span></span> | <span data-ttu-id="a3ab6-113">Value</span><span class="sxs-lookup"><span data-stu-id="a3ab6-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a3ab6-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3ab6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a3ab6-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a3ab6-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a3ab6-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3ab6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a3ab6-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a3ab6-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a3ab6-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3ab6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3ab6-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="a3ab6-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




