---
description: El método GetSwapInputs recupera un valor que indica si se intercambian las entradas de la transición.
ms.assetid: 84cb5c3d-7c3a-4c35-aac7-97d812d99a38
title: 'IAMTimelineTrans:: GetSwapInputs (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a2acdff1007bd26773ce495d024676632eee1767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691024"
---
# <a name="iamtimelinetransgetswapinputs-method"></a><span data-ttu-id="6fa47-103">IAMTimelineTrans:: GetSwapInputs (método)</span><span class="sxs-lookup"><span data-stu-id="6fa47-103">IAMTimelineTrans::GetSwapInputs method</span></span>

> [!Note]  
> <span data-ttu-id="6fa47-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="6fa47-104">\[Deprecated.</span></span> <span data-ttu-id="6fa47-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6fa47-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6fa47-106">El `GetSwapInputs` método recupera un valor que indica si se intercambian las entradas de la transición.</span><span class="sxs-lookup"><span data-stu-id="6fa47-106">The `GetSwapInputs` method retrieves a value that indicates whether the transition inputs are swapped.</span></span>

<span data-ttu-id="6fa47-107">De forma predeterminada, una transición va desde el compuesto de todas las capas de prioridad inferior hasta la capa en la que reside la transición.</span><span class="sxs-lookup"><span data-stu-id="6fa47-107">By default, a transition goes from the composite of all lower-priority layers to the layer where the transition resides.</span></span> <span data-ttu-id="6fa47-108">Puede invertir esta progresión, por lo que la transición va desde la capa en la que reside hasta el compuesto de capas de menor prioridad.</span><span class="sxs-lookup"><span data-stu-id="6fa47-108">You can reverse this progression, so the transition goes from the layer where it resides back to the composite of lower-priority layers.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fa47-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6fa47-109">Syntax</span></span>


```C++
HRESULT GetSwapInputs(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="6fa47-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6fa47-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fa47-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="6fa47-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="6fa47-112">Recibe un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="6fa47-112">Receives a Boolean value.</span></span> <span data-ttu-id="6fa47-113">Si el valor es **false**, la transición va desde el compuesto de todas las capas de prioridad más baja hasta la capa de transición.</span><span class="sxs-lookup"><span data-stu-id="6fa47-113">If the value is **FALSE**, the transition goes from the composite of all lower-priority layers to the transition layer.</span></span> <span data-ttu-id="6fa47-114">Si el valor es **true**, la transición va en la dirección opuesta.</span><span class="sxs-lookup"><span data-stu-id="6fa47-114">If the value is **TRUE**, the transition goes in the opposite direction.</span></span> <span data-ttu-id="6fa47-115">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="6fa47-115">The default value is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fa47-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6fa47-116">Return value</span></span>

<span data-ttu-id="6fa47-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="6fa47-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6fa47-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6fa47-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fa47-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6fa47-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6fa47-120">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="6fa47-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6fa47-121">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6fa47-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6fa47-122">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6fa47-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6fa47-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fa47-123">Requirements</span></span>



| <span data-ttu-id="6fa47-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fa47-124">Requirement</span></span> | <span data-ttu-id="6fa47-125">Value</span><span class="sxs-lookup"><span data-stu-id="6fa47-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa47-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6fa47-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6fa47-127"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fa47-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6fa47-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6fa47-128">Library</span></span><br/> | <dl> <span data-ttu-id="6fa47-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fa47-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fa47-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6fa47-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fa47-131">**Interfaz IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="6fa47-131">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="6fa47-132">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="6fa47-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




