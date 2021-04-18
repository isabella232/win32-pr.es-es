---
title: IWMPCdromBurn isAvailable (método)
description: El método isAvailable proporciona información acerca de la unidad de CD y el medio.
ms.assetid: 75e81f5f-5839-4012-b0b9-e77b3ca6f35c
keywords:
- isAvailable (método) Windows Media Player
- método isAvailable Windows Media Player, interfaz IWMPCdromBurn
- Interfaz IWMPCdromBurn Windows Media Player, isAvailable (método)
topic_type:
- apiref
api_name:
- IWMPCdromBurn.isAvailable
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d604cb9d9e170a3837fbd477db4c7ff309e1df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718830"
---
# <a name="iwmpcdromburnisavailable-method"></a><span data-ttu-id="93c20-106">IWMPCdromBurn:: isAvailable (método)</span><span class="sxs-lookup"><span data-stu-id="93c20-106">IWMPCdromBurn::isAvailable method</span></span>

<span data-ttu-id="93c20-107">El método **isavailable** proporciona información acerca de la unidad de CD y el medio.</span><span class="sxs-lookup"><span data-stu-id="93c20-107">The **isAvailable** method provides information about the CD drive and media.</span></span>

## <a name="syntax"></a><span data-ttu-id="93c20-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93c20-108">Syntax</span></span>


```CSharp
public System.Boolean isAvailable(
  System.String bstrItem
);
```


```VB

Public Function isAvailable( _
  ByVal bstrItem As System.String _
) As System.Boolean
Implements IWMPCdromBurn.isAvailable
```





## <a name="parameters"></a><span data-ttu-id="93c20-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93c20-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93c20-110">*bstrItem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="93c20-110">*bstrItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93c20-111">**System. String** que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="93c20-111">A **System.String** that contains one of the following values.</span></span>



| <span data-ttu-id="93c20-112">Value</span><span class="sxs-lookup"><span data-stu-id="93c20-112">Value</span></span> | <span data-ttu-id="93c20-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="93c20-113">Description</span></span>                 |
|-------|-----------------------------|
| <span data-ttu-id="93c20-114">Burn</span><span class="sxs-lookup"><span data-stu-id="93c20-114">Burn</span></span>  | <span data-ttu-id="93c20-115">La unidad es una grabadora de CD.</span><span class="sxs-lookup"><span data-stu-id="93c20-115">The drive is a CD burner.</span></span>   |
| <span data-ttu-id="93c20-116">Disco</span><span class="sxs-lookup"><span data-stu-id="93c20-116">Disc</span></span>  | <span data-ttu-id="93c20-117">Hay un CD en la unidad.</span><span class="sxs-lookup"><span data-stu-id="93c20-117">There is a CD in the drive.</span></span> |
| <span data-ttu-id="93c20-118">Borrar</span><span class="sxs-lookup"><span data-stu-id="93c20-118">Erase</span></span> | <span data-ttu-id="93c20-119">El CD se puede borrar.</span><span class="sxs-lookup"><span data-stu-id="93c20-119">The CD can be erased.</span></span>       |
| <span data-ttu-id="93c20-120">Escritura</span><span class="sxs-lookup"><span data-stu-id="93c20-120">Write</span></span> | <span data-ttu-id="93c20-121">Se puede escribir en el CD.</span><span class="sxs-lookup"><span data-stu-id="93c20-121">The CD can be written to.</span></span>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93c20-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93c20-122">Return value</span></span>

<span data-ttu-id="93c20-123">**System. Boolean** que indica el resultado.</span><span class="sxs-lookup"><span data-stu-id="93c20-123">A **System.Boolean** that indicates the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="93c20-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93c20-124">Requirements</span></span>



| <span data-ttu-id="93c20-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="93c20-125">Requirement</span></span> | <span data-ttu-id="93c20-126">Value</span><span class="sxs-lookup"><span data-stu-id="93c20-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93c20-127">Versión</span><span class="sxs-lookup"><span data-stu-id="93c20-127">Version</span></span><br/>   | <span data-ttu-id="93c20-128">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="93c20-128">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="93c20-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="93c20-129">Namespace</span></span><br/> | <span data-ttu-id="93c20-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="93c20-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="93c20-131">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="93c20-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="93c20-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="93c20-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93c20-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="93c20-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93c20-134">**Interfaz IWMPCdromBurn (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="93c20-134">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





