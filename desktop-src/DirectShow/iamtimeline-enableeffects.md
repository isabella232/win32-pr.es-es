---
description: El método EnableEffects habilita o deshabilita todos los efectos de la escala de tiempo. Si los efectos están deshabilitados, permanecen en la escala de tiempo pero no se representan.
ms.assetid: 5344cd49-6515-4211-9637-ca58219b3b56
title: 'IAMTimeline:: EnableEffects (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableEffects
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e090f115083e2d1433e60d7a8707ded9b89ba433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679384"
---
# <a name="iamtimelineenableeffects-method"></a><span data-ttu-id="706a0-104">IAMTimeline:: EnableEffects (método)</span><span class="sxs-lookup"><span data-stu-id="706a0-104">IAMTimeline::EnableEffects method</span></span>

> [!Note]  
> <span data-ttu-id="706a0-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="706a0-105">\[Deprecated.</span></span> <span data-ttu-id="706a0-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="706a0-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="706a0-107">El `EnableEffects` método habilita o deshabilita todos los efectos de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="706a0-107">The `EnableEffects` method enables or disables all effects in the timeline.</span></span> <span data-ttu-id="706a0-108">Si los efectos están deshabilitados, permanecen en la escala de tiempo pero no se representan.</span><span class="sxs-lookup"><span data-stu-id="706a0-108">If effects are disabled, they remain in the timeline but are not rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="706a0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="706a0-109">Syntax</span></span>


```C++
HRESULT EnableEffects(
   BOOL fEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="706a0-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="706a0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="706a0-111">*fEnabled*</span><span class="sxs-lookup"><span data-stu-id="706a0-111">*fEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="706a0-112">Valor booleano que especifica si se deben habilitar o deshabilitar los efectos.</span><span class="sxs-lookup"><span data-stu-id="706a0-112">Boolean value that specifies whether to enable or disable effects.</span></span> <span data-ttu-id="706a0-113">Si **es true**, se habilitan los efectos.</span><span class="sxs-lookup"><span data-stu-id="706a0-113">If **TRUE**, effects are enabled.</span></span> <span data-ttu-id="706a0-114">Si **es false**, los efectos están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="706a0-114">If **FALSE**, effects are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="706a0-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="706a0-115">Return value</span></span>

<span data-ttu-id="706a0-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="706a0-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="706a0-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="706a0-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="706a0-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="706a0-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="706a0-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="706a0-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="706a0-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="706a0-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="706a0-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="706a0-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="706a0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="706a0-122">Requirements</span></span>



| <span data-ttu-id="706a0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="706a0-123">Requirement</span></span> | <span data-ttu-id="706a0-124">Value</span><span class="sxs-lookup"><span data-stu-id="706a0-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="706a0-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="706a0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="706a0-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="706a0-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="706a0-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="706a0-127">Library</span></span><br/> | <dl> <span data-ttu-id="706a0-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="706a0-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="706a0-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="706a0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="706a0-130">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="706a0-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="706a0-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="706a0-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




