---
description: El método SetCutPoint establece la hora a la que la transición corta de un origen al siguiente, si la transición se representa como un corte.
ms.assetid: 2660f4a8-e249-45d7-8866-02a9f2ef52b8
title: 'IAMTimelineTrans:: SetCutPoint (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c1dad934d373a52b7e6c076c8c20dc8e1c6809ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690311"
---
# <a name="iamtimelinetranssetcutpoint-method"></a><span data-ttu-id="8d77b-103">IAMTimelineTrans:: SetCutPoint (método)</span><span class="sxs-lookup"><span data-stu-id="8d77b-103">IAMTimelineTrans::SetCutPoint method</span></span>

> [!Note]  
> <span data-ttu-id="8d77b-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="8d77b-104">\[Deprecated.</span></span> <span data-ttu-id="8d77b-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8d77b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8d77b-106">El `SetCutPoint` método establece la hora a la que la transición corta de un origen al siguiente, si la transición se representa como un corte.</span><span class="sxs-lookup"><span data-stu-id="8d77b-106">The `SetCutPoint` method sets the time at which the transition cuts from one source to the next, if the transition is rendered as a cut.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d77b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d77b-107">Syntax</span></span>


```C++
HRESULT SetCutPoint(
   REFERENCE_TIME TLTime
);
```



## <a name="parameters"></a><span data-ttu-id="8d77b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d77b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d77b-109">*TLTime*</span><span class="sxs-lookup"><span data-stu-id="8d77b-109">*TLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="8d77b-110">Punto de corte relativo al inicio de la transición, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="8d77b-110">Cut point relative to the start of the transition, in 100-nanosecond units.</span></span> <span data-ttu-id="8d77b-111">Si el valor está fuera de los límites de la transición, se trunca a la hora válida más cercana.</span><span class="sxs-lookup"><span data-stu-id="8d77b-111">If the value falls outside the bounds of the transition, it is truncated to the nearest valid time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d77b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d77b-112">Return value</span></span>

<span data-ttu-id="8d77b-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8d77b-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8d77b-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8d77b-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d77b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d77b-115">Remarks</span></span>

<span data-ttu-id="8d77b-116">De forma predeterminada, el punto de corte es el medio de la transición.</span><span class="sxs-lookup"><span data-stu-id="8d77b-116">By default, the cut-point is the middle of the transition.</span></span> <span data-ttu-id="8d77b-117">Por ejemplo, en una transición que abarca un segundo, el punto de corte predeterminado es de 0,5 segundos en la transición.</span><span class="sxs-lookup"><span data-stu-id="8d77b-117">For example, in a transition that spans one second, the default cut point is 0.5 seconds into the transition.</span></span>

> [!Note]  
> <span data-ttu-id="8d77b-118">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="8d77b-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8d77b-119">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8d77b-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8d77b-120">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8d77b-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8d77b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d77b-121">Requirements</span></span>



| <span data-ttu-id="8d77b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d77b-122">Requirement</span></span> | <span data-ttu-id="8d77b-123">Value</span><span class="sxs-lookup"><span data-stu-id="8d77b-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d77b-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d77b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8d77b-125"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d77b-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8d77b-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d77b-126">Library</span></span><br/> | <dl> <span data-ttu-id="8d77b-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d77b-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d77b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d77b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d77b-129">**Interfaz IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="8d77b-129">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="8d77b-130">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="8d77b-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




