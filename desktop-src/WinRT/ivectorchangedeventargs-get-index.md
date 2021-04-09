---
description: Obtiene la posición en el vector en el que se produjo el cambio.
ms.assetid: 00756d77-aae0-45f0-8bd4-cf68af9bdc7c
title: 'Método IVectorChangedEventArgs:: get_Index (IVectorChangedEventArgs. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_Index
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: 5c131567ec7fc2861ce11db9e5d7ec581f6f663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082126"
---
# <a name="ivectorchangedeventargsget_index-method"></a><span data-ttu-id="c490e-103">IVectorChangedEventArgs:: get \_ index (método)</span><span class="sxs-lookup"><span data-stu-id="c490e-103">IVectorChangedEventArgs::get\_Index method</span></span>

<span data-ttu-id="c490e-104">Obtiene la posición en el vector en el que se produjo el cambio.</span><span class="sxs-lookup"><span data-stu-id="c490e-104">Gets the position in the vector where the change occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="c490e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c490e-105">Syntax</span></span>


```C++
HRESULT get_Index(
  [out, retval] unsigned *value
);
```



## <a name="parameters"></a><span data-ttu-id="c490e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c490e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c490e-107">*valor* \[ de out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c490e-107">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c490e-108">Tipo: \**sin signo \** _</span><span class="sxs-lookup"><span data-stu-id="c490e-108">Type: \**unsigned\** _</span></span>

<span data-ttu-id="c490e-109">Posición de base cero del vector donde se produjo el cambio, si procede.</span><span class="sxs-lookup"><span data-stu-id="c490e-109">The zero-based position in the vector where the change occurred, if applicable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c490e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c490e-110">Return value</span></span>

<span data-ttu-id="c490e-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c490e-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c490e-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c490e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c490e-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c490e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c490e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c490e-114">Requirements</span></span>



| <span data-ttu-id="c490e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c490e-115">Requirement</span></span> | <span data-ttu-id="c490e-116">Value</span><span class="sxs-lookup"><span data-stu-id="c490e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c490e-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c490e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c490e-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c490e-118">Windows 8</span></span><br/>                                                                                 |
| <span data-ttu-id="c490e-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c490e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c490e-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c490e-120">Windows Server 2012</span></span><br/>                                                                       |
| <span data-ttu-id="c490e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c490e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c490e-122"><dt>IVectorChangedEventArgs. h</dt></span><span class="sxs-lookup"><span data-stu-id="c490e-122"><dt>IVectorChangedEventArgs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c490e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c490e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c490e-124">**IVectorChangedEventArgs**</span><span class="sxs-lookup"><span data-stu-id="c490e-124">**IVectorChangedEventArgs**</span></span>](ivectorchangedeventargs.md)
</dt> </dl>

 

 




