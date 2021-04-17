---
description: No se ha implementado el método GetCurrentSample.
ms.assetid: 0c903498-3c1d-4e95-a797-ca8cfded25f2
title: 'ISampleGrabber:: GetCurrentSample (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentSample
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9a21f50f84f030502cfd3243d36595e465e1b85b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680642"
---
# <a name="isamplegrabbergetcurrentsample-method"></a><span data-ttu-id="0f0e9-103">ISampleGrabber:: GetCurrentSample (método)</span><span class="sxs-lookup"><span data-stu-id="0f0e9-103">ISampleGrabber::GetCurrentSample method</span></span>

> [!Note]  
> <span data-ttu-id="0f0e9-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-104">\[Deprecated.</span></span> <span data-ttu-id="0f0e9-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0f0e9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0f0e9-106">El método `GetCurrentSample` no está implementado.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-106">The `GetCurrentSample` method is not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f0e9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f0e9-107">Syntax</span></span>


```C++
HRESULT GetCurrentSample(
   IMediaSample **ppSample
);
```



## <a name="parameters"></a><span data-ttu-id="0f0e9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f0e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f0e9-109">*ppSample*</span><span class="sxs-lookup"><span data-stu-id="0f0e9-109">*ppSample*</span></span> 
</dt> <dd>

<span data-ttu-id="0f0e9-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f0e9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f0e9-111">Return value</span></span>

<span data-ttu-id="0f0e9-112">Devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f0e9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f0e9-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0f0e9-114">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0f0e9-115">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0f0e9-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0f0e9-116">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0f0e9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f0e9-117">Requirements</span></span>



| <span data-ttu-id="0f0e9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f0e9-118">Requirement</span></span> | <span data-ttu-id="0f0e9-119">Value</span><span class="sxs-lookup"><span data-stu-id="0f0e9-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f0e9-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f0e9-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0f0e9-121"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f0e9-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0f0e9-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f0e9-122">Library</span></span><br/> | <dl> <span data-ttu-id="0f0e9-123"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f0e9-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f0e9-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f0e9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f0e9-125">Usar el enganche de ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f0e9-125">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="0f0e9-126">**Interfaz ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="0f0e9-126">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




