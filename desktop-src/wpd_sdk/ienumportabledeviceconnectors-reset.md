---
description: 'Método IEnumPortableDeviceConnectors::Reset: restablece la secuencia de enumeración al principio.'
ms.assetid: 1df1ff95-06ae-4e5e-8064-17f832c5f0b3
title: Método IEnumPortableDeviceConnectors::Reset (Devpkey.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Reset
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 10a356fbb8591568a9f99d9b92d681a46754a960
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083213"
---
# <a name="ienumportabledeviceconnectorsreset-method"></a><span data-ttu-id="198c7-103">IEnumPortableDeviceConnectors::Reset (Método)</span><span class="sxs-lookup"><span data-stu-id="198c7-103">IEnumPortableDeviceConnectors::Reset method</span></span>

<span data-ttu-id="198c7-104">El **método Reset** restablece la secuencia de enumeración al principio.</span><span class="sxs-lookup"><span data-stu-id="198c7-104">The **Reset** method resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="198c7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="198c7-105">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="198c7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="198c7-106">Parameters</span></span>

<span data-ttu-id="198c7-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="198c7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="198c7-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="198c7-108">Return value</span></span>

<span data-ttu-id="198c7-109">El método devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="198c7-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="198c7-110">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="198c7-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="198c7-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="198c7-111">Return code</span></span>                                                                          | <span data-ttu-id="198c7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="198c7-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="198c7-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="198c7-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="198c7-114">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="198c7-114">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="198c7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="198c7-115">Requirements</span></span>



| <span data-ttu-id="198c7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="198c7-116">Requirement</span></span> | <span data-ttu-id="198c7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="198c7-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="198c7-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="198c7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="198c7-119">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="198c7-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="198c7-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="198c7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="198c7-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="198c7-121">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="198c7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="198c7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="198c7-123"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="198c7-123"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="198c7-124">Idl</span><span class="sxs-lookup"><span data-stu-id="198c7-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="198c7-125"><dt>Portabledeviceconnectapi.idl</dt></span><span class="sxs-lookup"><span data-stu-id="198c7-125"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="198c7-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="198c7-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="198c7-127"><dt>PortableDeviceGuids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="198c7-127"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="198c7-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="198c7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="198c7-129">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="198c7-129">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




