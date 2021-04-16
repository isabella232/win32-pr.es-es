---
description: El método GetDuration recupera la duración de la escala de tiempo.
ms.assetid: d60269b8-597a-4ba4-932a-54b4a36e9a7a
title: 'IAMTimeline:: GetDuration (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDuration
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98257c40bf2072a2b8881a4744cdbe6d3a4e7df5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679475"
---
# <a name="iamtimelinegetduration-method"></a><span data-ttu-id="58916-103">IAMTimeline:: GetDuration (método)</span><span class="sxs-lookup"><span data-stu-id="58916-103">IAMTimeline::GetDuration method</span></span>

> [!Note]  
> <span data-ttu-id="58916-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="58916-104">\[Deprecated.</span></span> <span data-ttu-id="58916-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="58916-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="58916-106">El `GetDuration` método recupera la duración de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="58916-106">The `GetDuration` method retrieves the duration of the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="58916-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58916-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   REFERENCE_TIME *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="58916-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58916-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58916-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="58916-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="58916-110">Recibe la duración de la escala de tiempo, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="58916-110">Receives the duration of the timeline, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58916-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58916-111">Return value</span></span>

<span data-ttu-id="58916-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="58916-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="58916-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="58916-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="58916-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58916-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="58916-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="58916-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="58916-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="58916-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="58916-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="58916-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="58916-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58916-118">Requirements</span></span>



| <span data-ttu-id="58916-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="58916-119">Requirement</span></span> | <span data-ttu-id="58916-120">Value</span><span class="sxs-lookup"><span data-stu-id="58916-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58916-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58916-121">Header</span></span><br/>  | <dl> <span data-ttu-id="58916-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="58916-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="58916-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58916-123">Library</span></span><br/> | <dl> <span data-ttu-id="58916-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58916-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58916-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="58916-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58916-126">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="58916-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="58916-127">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="58916-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




