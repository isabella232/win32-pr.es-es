---
description: El método TransitionsEnabled determina si las transiciones están habilitadas.
ms.assetid: c961d8d7-4509-444b-a49f-6ab79fc31f7e
title: 'IAMTimeline:: TransitionsEnabled (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.TransitionsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7116ccf4ff2015934c9071f4ce2ef073656b89c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690617"
---
# <a name="iamtimelinetransitionsenabled-method"></a><span data-ttu-id="54ee8-103">IAMTimeline:: TransitionsEnabled (método)</span><span class="sxs-lookup"><span data-stu-id="54ee8-103">IAMTimeline::TransitionsEnabled method</span></span>

> [!Note]  
> <span data-ttu-id="54ee8-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="54ee8-104">\[Deprecated.</span></span> <span data-ttu-id="54ee8-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="54ee8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="54ee8-106">El método **TransitionsEnabled** determina si las transiciones están habilitadas.</span><span class="sxs-lookup"><span data-stu-id="54ee8-106">The **TransitionsEnabled** method determines whether transitions are enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="54ee8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54ee8-107">Syntax</span></span>


```C++
HRESULT TransitionsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="54ee8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54ee8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54ee8-109">*pfEnabled*</span><span class="sxs-lookup"><span data-stu-id="54ee8-109">*pfEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="54ee8-110">Recibe un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="54ee8-110">Receives a Boolean value.</span></span> <span data-ttu-id="54ee8-111">Si **es true**, las transiciones están habilitadas.</span><span class="sxs-lookup"><span data-stu-id="54ee8-111">If **TRUE**, transitions are enabled.</span></span> <span data-ttu-id="54ee8-112">De lo contrario, las transiciones están deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="54ee8-112">Otherwise, transitions are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54ee8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54ee8-113">Return value</span></span>

<span data-ttu-id="54ee8-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="54ee8-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="54ee8-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="54ee8-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="54ee8-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54ee8-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="54ee8-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="54ee8-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="54ee8-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="54ee8-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="54ee8-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="54ee8-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="54ee8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54ee8-120">Requirements</span></span>



| <span data-ttu-id="54ee8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="54ee8-121">Requirement</span></span> | <span data-ttu-id="54ee8-122">Value</span><span class="sxs-lookup"><span data-stu-id="54ee8-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54ee8-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54ee8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="54ee8-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="54ee8-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="54ee8-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="54ee8-125">Library</span></span><br/> | <dl> <span data-ttu-id="54ee8-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54ee8-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54ee8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="54ee8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54ee8-128">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="54ee8-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="54ee8-129">**IAMTimeline::EnableTransitions**</span><span class="sxs-lookup"><span data-stu-id="54ee8-129">**IAMTimeline::EnableTransitions**</span></span>](iamtimeline-enabletransitions.md)
</dt> <dt>

[<span data-ttu-id="54ee8-130">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="54ee8-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




