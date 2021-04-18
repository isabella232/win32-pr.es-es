---
description: Devuelve el tipo de dispositivo de hardware que representa el objeto de tableta, como el mouse, el lápiz o la entrada táctil.
ms.assetid: 693cb45f-958d-42e2-a3ee-a7cfcc72e5c3
title: 'ITablet2:: GetDeviceKind (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2.GetDeviceKind
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f20b1fe6a5a48196f6b3adc5982f2596d93f0863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720585"
---
# <a name="itablet2getdevicekind-method"></a><span data-ttu-id="c4390-103">ITablet2:: GetDeviceKind (método)</span><span class="sxs-lookup"><span data-stu-id="c4390-103">ITablet2::GetDeviceKind method</span></span>

<span data-ttu-id="c4390-104">Devuelve el tipo de dispositivo de hardware que representa el objeto de tableta, como el mouse, el lápiz o la entrada táctil.</span><span class="sxs-lookup"><span data-stu-id="c4390-104">Returns the type of hardware device the tablet object represents such as mouse, pen or touch.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4390-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4390-105">Syntax</span></span>


```C++
HRESULT GetDeviceKind(
  [out] TABLET_DEVICE_KIND *pKind
);
```



## <a name="parameters"></a><span data-ttu-id="c4390-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4390-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4390-107">*pKind* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c4390-107">*pKind* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4390-108">Valor de enumeración que indica el tipo de tableta, como el mouse, el lápiz o la entrada táctil.</span><span class="sxs-lookup"><span data-stu-id="c4390-108">Enumeration value that indicates the type of tablet such as mouse, pen or touch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4390-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4390-109">Return value</span></span>

<span data-ttu-id="c4390-110">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="c4390-110">This method can return one of these values.</span></span>



| <span data-ttu-id="c4390-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c4390-111">Return code</span></span>                                                                            | <span data-ttu-id="c4390-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4390-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="c4390-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c4390-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="c4390-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c4390-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="c4390-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="c4390-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="c4390-116">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="c4390-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c4390-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4390-117">Remarks</span></span>

<span data-ttu-id="c4390-118">Esta interfaz y este método se introdujeron en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c4390-118">This interface and method were introduced in Windows Vista.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4390-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4390-119">Requirements</span></span>



| <span data-ttu-id="c4390-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4390-120">Requirement</span></span> | <span data-ttu-id="c4390-121">Value</span><span class="sxs-lookup"><span data-stu-id="c4390-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4390-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4390-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c4390-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c4390-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c4390-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4390-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c4390-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c4390-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c4390-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c4390-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4390-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c4390-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4390-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4390-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4390-129">**Interfaz ITablet2**</span><span class="sxs-lookup"><span data-stu-id="c4390-129">**ITablet2 Interface**</span></span>](itablet2.md)
</dt> <dt>

[<span data-ttu-id="c4390-130">**\_Enumeración de tipo de dispositivo de tableta \_**</span><span class="sxs-lookup"><span data-stu-id="c4390-130">**TABLET\_DEVICE\_KIND Enumeration**</span></span>](tablet-device-kind.md)
</dt> <dt>

[<span data-ttu-id="c4390-131">**Interfaz ITablet**</span><span class="sxs-lookup"><span data-stu-id="c4390-131">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




