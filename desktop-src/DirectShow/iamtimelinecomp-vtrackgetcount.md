---
description: El método VTrackGetCount recupera el número de pistas virtuales contenidas en la composición.
ms.assetid: a8117b06-4f42-45da-9b93-f547cb70aa5d
title: 'IAMTimelineComp:: VTrackGetCount (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackGetCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 36800381ce50ea60d5252841d9731b2657fc22cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690838"
---
# <a name="iamtimelinecompvtrackgetcount-method"></a><span data-ttu-id="4e519-103">IAMTimelineComp:: VTrackGetCount (método)</span><span class="sxs-lookup"><span data-stu-id="4e519-103">IAMTimelineComp::VTrackGetCount method</span></span>

> [!Note]  
> <span data-ttu-id="4e519-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="4e519-104">\[Deprecated.</span></span> <span data-ttu-id="4e519-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4e519-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4e519-106">El `VTrackGetCount` método recupera el número de pistas virtuales contenidas en la composición.</span><span class="sxs-lookup"><span data-stu-id="4e519-106">The `VTrackGetCount` method retrieves the number of virtual tracks contained in the composition.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e519-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e519-107">Syntax</span></span>


```C++
HRESULT VTrackGetCount(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="4e519-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e519-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e519-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="4e519-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="4e519-110">Recibe el número de pistas virtuales.</span><span class="sxs-lookup"><span data-stu-id="4e519-110">Receives the number of virtual tracks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e519-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e519-111">Return value</span></span>

<span data-ttu-id="4e519-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4e519-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4e519-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4e519-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e519-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e519-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4e519-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="4e519-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4e519-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4e519-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4e519-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4e519-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4e519-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e519-118">Requirements</span></span>



| <span data-ttu-id="4e519-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e519-119">Requirement</span></span> | <span data-ttu-id="4e519-120">Value</span><span class="sxs-lookup"><span data-stu-id="4e519-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e519-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e519-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4e519-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e519-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4e519-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e519-123">Library</span></span><br/> | <dl> <span data-ttu-id="4e519-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e519-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e519-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e519-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e519-126">**Interfaz IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="4e519-126">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="4e519-127">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="4e519-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




