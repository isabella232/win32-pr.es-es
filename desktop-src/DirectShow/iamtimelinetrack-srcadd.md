---
description: El método SrcAdd agrega un origen a la pista.
ms.assetid: 71c62e92-02d6-4c6f-8121-2052d6cc832c
title: 'IAMTimelineTrack:: SrcAdd (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.SrcAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3d1d727fb6a99e3dea9ec2659838df1bfcd392b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690112"
---
# <a name="iamtimelinetracksrcadd-method"></a><span data-ttu-id="59e1d-103">IAMTimelineTrack:: SrcAdd (método)</span><span class="sxs-lookup"><span data-stu-id="59e1d-103">IAMTimelineTrack::SrcAdd method</span></span>

> [!Note]  
> <span data-ttu-id="59e1d-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="59e1d-104">\[Deprecated.</span></span> <span data-ttu-id="59e1d-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="59e1d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="59e1d-106">El `SrcAdd` método agrega un origen a la pista.</span><span class="sxs-lookup"><span data-stu-id="59e1d-106">The `SrcAdd` method adds a source to the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="59e1d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59e1d-107">Syntax</span></span>


```C++
HRESULT SrcAdd(
   IAMTimelineObj *pSrc
);
```



## <a name="parameters"></a><span data-ttu-id="59e1d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59e1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59e1d-109">*pSrc*</span><span class="sxs-lookup"><span data-stu-id="59e1d-109">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="59e1d-110">Puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="59e1d-110">Pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59e1d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59e1d-111">Return value</span></span>

<span data-ttu-id="59e1d-112">Devuelve S \_ correcto si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="59e1d-112">Returns S\_OK if successful.</span></span> <span data-ttu-id="59e1d-113">Devuelve E \_ nointerface si el objeto no es un objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="59e1d-113">Returns E\_NOINTERFACE if the object is not a source object.</span></span> <span data-ttu-id="59e1d-114">De lo contrario, devuelve un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="59e1d-114">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="59e1d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59e1d-115">Remarks</span></span>

<span data-ttu-id="59e1d-116">Establezca las horas de inicio y detención del origen antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="59e1d-116">Set the source's start and stop times before calling this method.</span></span> <span data-ttu-id="59e1d-117">(Llame a [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md)).</span><span class="sxs-lookup"><span data-stu-id="59e1d-117">(Call [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md).)</span></span>

<span data-ttu-id="59e1d-118">Actualmente, DES no puede representar simultáneamente más de 75 orígenes que se comprimieron con códecs de administrador de compresión de vídeo (VCM).</span><span class="sxs-lookup"><span data-stu-id="59e1d-118">Currently, DES cannot simultaneously render more than 75 sources that were compressed with Video Compression Manager (VCM) codecs.</span></span> <span data-ttu-id="59e1d-119">Además, si el proyecto como un conjunto contiene más de 75 tales orígenes, debe usar reconexión dinámica o DES no puede obtener una vista previa del proyecto.</span><span class="sxs-lookup"><span data-stu-id="59e1d-119">Also, if the project as a whole contains more than 75 such sources, you must use dynamic reconnection or DES cannot preview the project.</span></span> <span data-ttu-id="59e1d-120">Para obtener más información, vea [**IRenderEngine:: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span><span class="sxs-lookup"><span data-stu-id="59e1d-120">For more information, see [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

> [!Note]  
> <span data-ttu-id="59e1d-121">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="59e1d-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="59e1d-122">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="59e1d-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="59e1d-123">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="59e1d-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="59e1d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59e1d-124">Requirements</span></span>



| <span data-ttu-id="59e1d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="59e1d-125">Requirement</span></span> | <span data-ttu-id="59e1d-126">Value</span><span class="sxs-lookup"><span data-stu-id="59e1d-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59e1d-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59e1d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="59e1d-128"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="59e1d-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="59e1d-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59e1d-129">Library</span></span><br/> | <dl> <span data-ttu-id="59e1d-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59e1d-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59e1d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="59e1d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59e1d-132">**Interfaz IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="59e1d-132">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="59e1d-133">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="59e1d-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




