---
description: Especifica el modo de control de división. Los valores válidos son 0, 1, y 2.
ms.assetid: 5269DB79-639C-4F67-B885-BF1274CDB635
title: Propiedad CODECAPI_AVEncSliceControlMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0aef928a3938b2f0756d2e84b6836da194823dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000869"
---
# <a name="codecapi_avencslicecontrolmode-property"></a><span data-ttu-id="ca115-104">\_Propiedad AVEncSliceControlMode de CODECAPI</span><span class="sxs-lookup"><span data-stu-id="ca115-104">CODECAPI\_AVEncSliceControlMode property</span></span>

<span data-ttu-id="ca115-105">Especifica el modo de control de división.</span><span class="sxs-lookup"><span data-stu-id="ca115-105">Specifies the slice control mode.</span></span> <span data-ttu-id="ca115-106">Los valores válidos son 0, 1, y 2.</span><span class="sxs-lookup"><span data-stu-id="ca115-106">Valid values are 0, 1, and 2.</span></span>

## <a name="data-type"></a><span data-ttu-id="ca115-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ca115-107">Data type</span></span>

<span data-ttu-id="ca115-108">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="ca115-108">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ca115-109">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="ca115-109">Property GUID</span></span>

<span data-ttu-id="ca115-110">**CODECAPI \_ AVEncSliceControlMode**</span><span class="sxs-lookup"><span data-stu-id="ca115-110">**CODECAPI\_AVEncSliceControlMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="ca115-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ca115-111">Property value</span></span>

<span data-ttu-id="ca115-112">Valores de modo de control de segmento:</span><span class="sxs-lookup"><span data-stu-id="ca115-112">Slice control mode values:</span></span>



| <span data-ttu-id="ca115-113">Value</span><span class="sxs-lookup"><span data-stu-id="ca115-113">Value</span></span>                                                                        | <span data-ttu-id="ca115-114">Significado</span><span class="sxs-lookup"><span data-stu-id="ca115-114">Meaning</span></span>                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ca115-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ca115-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="ca115-116">Si se establece este valor en 0, se indica que la propiedad [ \_ AVEncSliceControlSize de CODECAPI](codecapi-avencslicecontrolsize.md) especificará el tamaño del segmento en unidades de macrobloques por segmento.</span><span class="sxs-lookup"><span data-stu-id="ca115-116">Setting this value to 0 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of macroblocks per slice.</span></span><br/>     |
| <dl> <span data-ttu-id="ca115-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ca115-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="ca115-118">Si se establece este valor en 1, se indica que la propiedad [ \_ AVEncSliceControlSize de CODECAPI](codecapi-avencslicecontrolsize.md) especificará el tamaño del segmento en unidades de bits por segmento.</span><span class="sxs-lookup"><span data-stu-id="ca115-118">Setting this value to 1 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of bits per slice.</span></span><br/>            |
| <dl> <span data-ttu-id="ca115-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ca115-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="ca115-120">Si se establece este valor en 2, se indica que la propiedad [ \_ AVEncSliceControlSize de CODECAPI](codecapi-avencslicecontrolsize.md) especificará el tamaño del sector en unidades de adaptativo macrobloque filas por segmento.</span><span class="sxs-lookup"><span data-stu-id="ca115-120">Setting this value to 2 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of macroblock rows per slice.</span></span><br/> |



 

<span data-ttu-id="ca115-121">El codificador devuelve los valores que admite.</span><span class="sxs-lookup"><span data-stu-id="ca115-121">The encoder returns the values that it supports.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca115-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca115-122">Remarks</span></span>

<span data-ttu-id="ca115-123">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="ca115-123">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="ca115-124">Se recomienda que el codificador admita [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)y [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="ca115-124">It is recommended that the encoder supports [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="ca115-125">Si no se llama a [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) para CODECAPI \_ AVEncSliceControlMode, [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) para CODECAPI \_ AVEncSliceControlMode puede devolver **VFW \_ E \_ CODECAPI \_ ningún \_ \_ valor actual**.</span><span class="sxs-lookup"><span data-stu-id="ca115-125">If [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) is not called for CODECAPI\_AVEncSliceControlMode, [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) for CODECAPI\_AVEncSliceControlMode can return **VFW\_E\_CODECAPI\_NO\_CURRENT\_VALUE**.</span></span> <span data-ttu-id="ca115-126">[**GetDefaultValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) puede devolver **VFW \_ E \_ CODECAPI \_ no \_ default** para CODECAPI \_ AVEncSliceControlMode.</span><span class="sxs-lookup"><span data-stu-id="ca115-126">[**GetDefaultValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) may return **VFW\_E\_CODECAPI\_NO\_DEFAULT** for CODECAPI\_AVEncSliceControlMode.</span></span>

<span data-ttu-id="ca115-127">El valor predeterminado recomendado es 2 (tamaño en MB fila por segmento).</span><span class="sxs-lookup"><span data-stu-id="ca115-127">Recommended default value is 2 (size in MB row per slice).</span></span>

<span data-ttu-id="ca115-128">Se trata de una API estática, lo que significa que la aplicación ha logrado cambiar esto mientras el codificador se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="ca115-128">This is a static API, which means the application won t change this while the encoder is running.</span></span>

## <a name="examples"></a><span data-ttu-id="ca115-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ca115-129">Examples</span></span>


```C++
if (pCodecAPI->IsSupported(&CODECAPI_AVEncSliceControlMode) == S_OK) {                
     VARIANT var;
     var.vt = VT_UI4;
     var.ulVal =ulSliceMode;
     pCodecAPI->SetValue(&CODECAPI_AVEncSliceControlMode, &var);
}
```



## <a name="requirements"></a><span data-ttu-id="ca115-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca115-130">Requirements</span></span>



| <span data-ttu-id="ca115-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca115-131">Requirement</span></span> | <span data-ttu-id="ca115-132">Value</span><span class="sxs-lookup"><span data-stu-id="ca115-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca115-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca115-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ca115-134">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="ca115-134">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="ca115-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca115-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ca115-136">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="ca115-136">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ca115-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca115-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca115-138"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca115-138"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca115-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca115-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca115-140">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ca115-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

