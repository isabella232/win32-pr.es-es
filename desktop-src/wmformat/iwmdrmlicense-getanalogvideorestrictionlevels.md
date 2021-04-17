---
title: Método IWMDRMLicense GetAnalogVideoRestrictionLevels (wmdrmsdk. h)
description: El método GetAnalogVideoRestrictionLevels recupera todas las restricciones de vídeo analógico establecidas en la licencia actual.
ms.assetid: cf0ac7c0-236d-4d60-8850-81dc6754cf01
keywords:
- Método GetAnalogVideoRestrictionLevels formato de Windows Media
- Método GetAnalogVideoRestrictionLevels formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método GetAnalogVideoRestrictionLevels
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetAnalogVideoRestrictionLevels
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a168f25381b807cc8c0cd17f7ba6764c3591513
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708894"
---
# <a name="iwmdrmlicensegetanalogvideorestrictionlevels-method"></a><span data-ttu-id="e3fb5-106">IWMDRMLicense:: GetAnalogVideoRestrictionLevels (método)</span><span class="sxs-lookup"><span data-stu-id="e3fb5-106">IWMDRMLicense::GetAnalogVideoRestrictionLevels method</span></span>

<span data-ttu-id="e3fb5-107">El método **GetAnalogVideoRestrictionLevels** recupera todas las restricciones de vídeo analógico establecidas en la licencia actual.</span><span class="sxs-lookup"><span data-stu-id="e3fb5-107">The **GetAnalogVideoRestrictionLevels** method retrieves all analog video restrictions set on the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3fb5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3fb5-108">Syntax</span></span>


```C++
HRESULT GetAnalogVideoRestrictionLevels(
  [out]     WMDRM_ANALOG_VIDEO_RESTRICTIONS rgAnalogVideoRestrictions[],
  [in, out] DWORD                           *pcRestrictions
);
```



## <a name="parameters"></a><span data-ttu-id="e3fb5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3fb5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3fb5-110">*\[ rgAnalogVideoRestrictions \]* \[fuera de\]</span><span class="sxs-lookup"><span data-stu-id="e3fb5-110">*rgAnalogVideoRestrictions\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3fb5-111">Recibe una matriz de estructuras de [**\_ \_ \_ restricciones de vídeo analógico WMDRM**](wmdrm-analog-video-restrictions.md) .</span><span class="sxs-lookup"><span data-stu-id="e3fb5-111">Receives an array of [**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS**](wmdrm-analog-video-restrictions.md) structures.</span></span> <span data-ttu-id="e3fb5-112">Establezca en **null** para obtener el número de elementos de la matriz en *pcResctrictions*.</span><span class="sxs-lookup"><span data-stu-id="e3fb5-112">Set to **NULL** to get the number of elements in the array in *pcResctrictions*.</span></span>

</dd> <dt>

<span data-ttu-id="e3fb5-113">*pcRestrictions* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e3fb5-113">*pcRestrictions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3fb5-114">Número de elementos de la matriz de restricciones.</span><span class="sxs-lookup"><span data-stu-id="e3fb5-114">The number of elements in the array of restrictions.</span></span> <span data-ttu-id="e3fb5-115">Si *rgAnalogVideoRestrictions* se establece en **null**, este valor se establece en el número de elementos necesarios en la matriz.</span><span class="sxs-lookup"><span data-stu-id="e3fb5-115">If *rgAnalogVideoRestrictions* is set to **NULL**, this value is set to the number of elements needed in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3fb5-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3fb5-116">Return value</span></span>

<span data-ttu-id="e3fb5-117">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e3fb5-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e3fb5-118">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="e3fb5-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e3fb5-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e3fb5-119">Return code</span></span>                                                                          | <span data-ttu-id="e3fb5-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3fb5-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e3fb5-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e3fb5-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e3fb5-122">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="e3fb5-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e3fb5-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3fb5-123">Remarks</span></span>

<span data-ttu-id="e3fb5-124">Debe asignar memoria para la matriz de restricciones.</span><span class="sxs-lookup"><span data-stu-id="e3fb5-124">You must allocate memory for the array of restrictions.</span></span> <span data-ttu-id="e3fb5-125">Para ello, llame primero al método con *rgAnalogVideoRestrictions* establecido en **null**, que establecerá el valor de *pcRestrictions* en el número de elementos necesarios.</span><span class="sxs-lookup"><span data-stu-id="e3fb5-125">To do so, first call the method with *rgAnalogVideoRestrictions* set to **NULL**, which will set the value at *pcRestrictions* to the number of required elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3fb5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3fb5-126">Requirements</span></span>



| <span data-ttu-id="e3fb5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3fb5-127">Requirement</span></span> | <span data-ttu-id="e3fb5-128">Value</span><span class="sxs-lookup"><span data-stu-id="e3fb5-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3fb5-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3fb5-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e3fb5-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3fb5-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="e3fb5-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3fb5-131">Library</span></span><br/> | <dl> <span data-ttu-id="e3fb5-132"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3fb5-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3fb5-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3fb5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3fb5-134">**Interfaz IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="e3fb5-134">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





