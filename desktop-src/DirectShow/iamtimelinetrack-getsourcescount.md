---
description: El método GetSourcesCount recupera el número de orígenes de la pista.
ms.assetid: eb7f249f-355f-454d-9fe6-c3271fd13fc7
title: 'IAMTimelineTrack:: GetSourcesCount (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSourcesCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0e143b16e5cdc1e193760c0b97846be07eb72c0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690122"
---
# <a name="iamtimelinetrackgetsourcescount-method"></a><span data-ttu-id="d22ab-103">IAMTimelineTrack:: GetSourcesCount (método)</span><span class="sxs-lookup"><span data-stu-id="d22ab-103">IAMTimelineTrack::GetSourcesCount method</span></span>

> [!Note]  
> <span data-ttu-id="d22ab-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="d22ab-104">\[Deprecated.</span></span> <span data-ttu-id="d22ab-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d22ab-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d22ab-106">El `GetSourcesCount` método recupera el número de orígenes de la pista.</span><span class="sxs-lookup"><span data-stu-id="d22ab-106">The `GetSourcesCount` method retrieves the number of sources in the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="d22ab-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d22ab-107">Syntax</span></span>


```C++
HRESULT GetSourcesCount(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="d22ab-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d22ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d22ab-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="d22ab-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="d22ab-110">Recibe el número de orígenes de la pista.</span><span class="sxs-lookup"><span data-stu-id="d22ab-110">Receives the number of sources in the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d22ab-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d22ab-111">Return value</span></span>

<span data-ttu-id="d22ab-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d22ab-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d22ab-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d22ab-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d22ab-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d22ab-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d22ab-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="d22ab-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d22ab-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d22ab-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d22ab-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d22ab-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d22ab-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d22ab-118">Requirements</span></span>



| <span data-ttu-id="d22ab-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d22ab-119">Requirement</span></span> | <span data-ttu-id="d22ab-120">Value</span><span class="sxs-lookup"><span data-stu-id="d22ab-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d22ab-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d22ab-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d22ab-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d22ab-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d22ab-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d22ab-123">Library</span></span><br/> | <dl> <span data-ttu-id="d22ab-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d22ab-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d22ab-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d22ab-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d22ab-126">**Interfaz IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="d22ab-126">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="d22ab-127">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="d22ab-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




