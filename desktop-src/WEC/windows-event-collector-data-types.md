---
title: Tipos de datos del recopilador de eventos de Windows (Evcoll. h)
description: Los tipos de datos del recopilador de eventos de Windows se usan como tipos de variables de objeto de suscripción de eventos, tipos de parámetros de función y tipos de valor devueltos de función.
ms.assetid: b78bdaf8-e034-40fe-acf8-632313e4fd94
ms.tgt_platform: multiple
keywords:
- EC_HANDLE
- EC_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ccec141317644aa091eac44033b87b9e4495ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695853"
---
# <a name="windows-event-collector-data-types"></a><span data-ttu-id="a42c0-105">Tipos de datos del recopilador de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="a42c0-105">Windows Event Collector Data Types</span></span>

<span data-ttu-id="a42c0-106">Los tipos de datos del recopilador de eventos de Windows se usan como tipos de variables de objeto de suscripción de eventos, tipos de parámetros de función y tipos de valor devueltos de función.</span><span class="sxs-lookup"><span data-stu-id="a42c0-106">The data types for the Windows Event Collector are used as event subscription object variable types, function parameter types, and function return types.</span></span>


```C++
typedef HANDLE EC_HANDLE;
typedef HANDLE EC_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

<span data-ttu-id="a42c0-107">**identificador de EC \_**</span><span class="sxs-lookup"><span data-stu-id="a42c0-107">**EC\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="a42c0-108">Identificador de un objeto de suscripción.</span><span class="sxs-lookup"><span data-stu-id="a42c0-108">Handle to a subscription object.</span></span> <span data-ttu-id="a42c0-109">Se utiliza para representar una suscripción del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="a42c0-109">Used to represent an event collector subscription.</span></span>

</dd> <dt>

<span data-ttu-id="a42c0-110">**\_identificador de \_ propiedad de matriz de objetos de EC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a42c0-110">**EC\_OBJECT\_ARRAY\_PROPERTY\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="a42c0-111">Identificador de una matriz de valores de propiedad para los orígenes de eventos de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="a42c0-111">Handle to an array of property values for the event sources of a subscription.</span></span> <span data-ttu-id="a42c0-112">El método [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) devuelve el identificador de matriz cuando el valor de **EcSubscriptionEventSources** se pasa al parámetro *PropertyId* .</span><span class="sxs-lookup"><span data-stu-id="a42c0-112">The array handle is returned by the [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) method when the **EcSubscriptionEventSources** value is passed into the *PropertyId* parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a42c0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a42c0-113">Requirements</span></span>



| <span data-ttu-id="a42c0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a42c0-114">Requirement</span></span> | <span data-ttu-id="a42c0-115">Value</span><span class="sxs-lookup"><span data-stu-id="a42c0-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a42c0-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a42c0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a42c0-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a42c0-117">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="a42c0-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a42c0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a42c0-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a42c0-119">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="a42c0-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a42c0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a42c0-121"><dt>Evcoll. h</dt></span><span class="sxs-lookup"><span data-stu-id="a42c0-121"><dt>Evcoll.h</dt></span></span> </dl> |



 

 





