---
description: Obtiene el tipo de cambio que se produjo en el vector.
ms.assetid: 213f4794-b972-44e3-a400-8a24b1583ddd
title: 'Método IVectorChangedEventArgs:: get_CollectionChange (IVectorChangedEventArgs. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_CollectionChange
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: a843574bcaf93ec524173ba76800cc15012c89fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275410"
---
# <a name="ivectorchangedeventargsget_collectionchange-method"></a><span data-ttu-id="058ad-103">IVectorChangedEventArgs:: get \_ CollectionChange (método)</span><span class="sxs-lookup"><span data-stu-id="058ad-103">IVectorChangedEventArgs::get\_CollectionChange method</span></span>

<span data-ttu-id="058ad-104">Obtiene el tipo de cambio que se produjo en el vector.</span><span class="sxs-lookup"><span data-stu-id="058ad-104">Gets the type of change that occurred in the vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="058ad-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="058ad-105">Syntax</span></span>


```C++
HRESULT get_CollectionChange(
  [out, retval] CollectionChange *value
);
```



## <a name="parameters"></a><span data-ttu-id="058ad-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="058ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="058ad-107">*valor* \[ de out, retval\]</span><span class="sxs-lookup"><span data-stu-id="058ad-107">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="058ad-108">Tipo: \**CollectionChange \** _</span><span class="sxs-lookup"><span data-stu-id="058ad-108">Type: \**CollectionChange\** _</span></span>

<span data-ttu-id="058ad-109">Un valor de la enumeración [_ *CollectionChange* \*](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) que describe el cambio.</span><span class="sxs-lookup"><span data-stu-id="058ad-109">A value from the [_ *CollectionChange*\*](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) enumeration that describes the change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="058ad-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="058ad-110">Return value</span></span>

<span data-ttu-id="058ad-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="058ad-111">Type: **HRESULT**</span></span>

<span data-ttu-id="058ad-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="058ad-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="058ad-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="058ad-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="058ad-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="058ad-114">Requirements</span></span>



| <span data-ttu-id="058ad-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="058ad-115">Requirement</span></span> | <span data-ttu-id="058ad-116">Value</span><span class="sxs-lookup"><span data-stu-id="058ad-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="058ad-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="058ad-117">Minimum supported client</span></span><br/> | <span data-ttu-id="058ad-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="058ad-118">Windows 8</span></span><br/>                                                                                 |
| <span data-ttu-id="058ad-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="058ad-119">Minimum supported server</span></span><br/> | <span data-ttu-id="058ad-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="058ad-120">Windows Server 2012</span></span><br/>                                                                       |
| <span data-ttu-id="058ad-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="058ad-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="058ad-122"><dt>IVectorChangedEventArgs. h</dt></span><span class="sxs-lookup"><span data-stu-id="058ad-122"><dt>IVectorChangedEventArgs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="058ad-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="058ad-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="058ad-124">**IVectorChangedEventArgs**</span><span class="sxs-lookup"><span data-stu-id="058ad-124">**IVectorChangedEventArgs**</span></span>](ivectorchangedeventargs.md)
</dt> </dl>

 

 
