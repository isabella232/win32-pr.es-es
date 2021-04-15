---
description: El método GetNextSrcEx recupera el siguiente origen después del origen especificado.
ms.assetid: cda3d079-eeb5-42a9-8854-5c90ae0e2c07
title: 'IAMTimelineTrack:: GetNextSrcEx (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrcEx
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 274a4f6800d995e2b456dbd55adf81cf82aa84a9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690124"
---
# <a name="iamtimelinetrackgetnextsrcex-method"></a><span data-ttu-id="b88e2-103">IAMTimelineTrack:: GetNextSrcEx (método)</span><span class="sxs-lookup"><span data-stu-id="b88e2-103">IAMTimelineTrack::GetNextSrcEx method</span></span>

> [!Note]  
> <span data-ttu-id="b88e2-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="b88e2-104">\[Deprecated.</span></span> <span data-ttu-id="b88e2-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b88e2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b88e2-106">El `GetNextSrcEx` método recupera el siguiente origen después del origen especificado.</span><span class="sxs-lookup"><span data-stu-id="b88e2-106">The `GetNextSrcEx` method retrieves the next source after the specified source.</span></span>

## <a name="syntax"></a><span data-ttu-id="b88e2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b88e2-107">Syntax</span></span>


```C++
HRESULT GetNextSrcEx(
        IAMTimelineObj *pLast,
  [out] IAMTimelineObj **ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="b88e2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b88e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b88e2-109">*pLast*</span><span class="sxs-lookup"><span data-stu-id="b88e2-109">*pLast*</span></span> 
</dt> <dd>

<span data-ttu-id="b88e2-110">Puntero al objeto de origen anterior o **null** para recuperar el primer origen de la pista.</span><span class="sxs-lookup"><span data-stu-id="b88e2-110">Pointer to the previous source object, or **NULL** to retrieve the first source in the track.</span></span>

</dd> <dt>

<span data-ttu-id="b88e2-111">*ppNext* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b88e2-111">*ppNext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b88e2-112">Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del siguiente objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="b88e2-112">Receives a pointer to the next source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b88e2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b88e2-113">Return value</span></span>

<span data-ttu-id="b88e2-114">Devuelve S \_ OK si el método recupera un origen o s \_ false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b88e2-114">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b88e2-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b88e2-115">Remarks</span></span>

<span data-ttu-id="b88e2-116">Si el método devuelve S \_ correcto, la interfaz **IAMTimelineObj** que devuelve tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="b88e2-116">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="b88e2-117">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="b88e2-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="b88e2-118">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="b88e2-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b88e2-119">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b88e2-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b88e2-120">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b88e2-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b88e2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b88e2-121">Requirements</span></span>



| <span data-ttu-id="b88e2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b88e2-122">Requirement</span></span> | <span data-ttu-id="b88e2-123">Value</span><span class="sxs-lookup"><span data-stu-id="b88e2-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b88e2-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b88e2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b88e2-125"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="b88e2-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b88e2-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b88e2-126">Library</span></span><br/> | <dl> <span data-ttu-id="b88e2-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b88e2-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b88e2-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b88e2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b88e2-129">**Interfaz IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="b88e2-129">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="b88e2-130">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="b88e2-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




