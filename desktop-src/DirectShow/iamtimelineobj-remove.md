---
description: El método Remove quita este objeto de la escala de tiempo (incluidos los subobjetos pero no los elementos secundarios) para volver a insertarlo en otro lugar.
ms.assetid: 118a08a5-abba-47df-8aeb-42ce8c8ed2ba
title: 'IAMTimelineObj:: Remove (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.Remove
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a3559787dfdacc68130dcaef073f32d07d4a0df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690729"
---
# <a name="iamtimelineobjremove-method"></a><span data-ttu-id="4b711-103">IAMTimelineObj:: Remove (método)</span><span class="sxs-lookup"><span data-stu-id="4b711-103">IAMTimelineObj::Remove method</span></span>

> [!Note]  
> <span data-ttu-id="4b711-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="4b711-104">\[Deprecated.</span></span> <span data-ttu-id="4b711-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4b711-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4b711-106">El `Remove` método quita este objeto de la escala de tiempo (incluidos los subobjetos pero no los elementos secundarios) para volver a insertar en cualquier lugar.</span><span class="sxs-lookup"><span data-stu-id="4b711-106">The `Remove` method removes this object from the timeline (including subobjects but not children), for reinsertion elsewhere.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b711-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b711-107">Syntax</span></span>


```C++
HRESULT Remove();
```



## <a name="parameters"></a><span data-ttu-id="4b711-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b711-108">Parameters</span></span>

<span data-ttu-id="4b711-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4b711-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b711-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b711-110">Return value</span></span>

<span data-ttu-id="4b711-111">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4b711-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4b711-112">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4b711-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b711-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b711-113">Remarks</span></span>

<span data-ttu-id="4b711-114">Llame a este método solo si la aplicación volverá a insertar inmediatamente el objeto en la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="4b711-114">Call this method only if the application will immediately insert the object back into the timeline.</span></span> <span data-ttu-id="4b711-115">Se trata de una operación no válida para llamar a este método sin volver a insertar el objeto.</span><span class="sxs-lookup"><span data-stu-id="4b711-115">It is an invalid operation to call this method without then reinserting the object.</span></span> <span data-ttu-id="4b711-116">Para quitar un objeto de forma permanente, llame a [**IAMTimelineObj:: RemoveAll**](iamtimelineobj-removeall.md).</span><span class="sxs-lookup"><span data-stu-id="4b711-116">To remove an object permanently, call [**IAMTimelineObj::RemoveAll**](iamtimelineobj-removeall.md).</span></span>

> [!Note]  
> <span data-ttu-id="4b711-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="4b711-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4b711-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4b711-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4b711-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4b711-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4b711-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b711-120">Requirements</span></span>



| <span data-ttu-id="4b711-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b711-121">Requirement</span></span> | <span data-ttu-id="4b711-122">Value</span><span class="sxs-lookup"><span data-stu-id="4b711-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b711-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b711-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4b711-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b711-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4b711-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b711-125">Library</span></span><br/> | <dl> <span data-ttu-id="4b711-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b711-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b711-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b711-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b711-128">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="4b711-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="4b711-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="4b711-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




