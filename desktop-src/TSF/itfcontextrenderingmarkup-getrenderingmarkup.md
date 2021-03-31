---
title: ITfContextRenderingMarkup GetRenderingMarkup, método
description: El método ITfContextRenderingMarkup GetRenderingMarkup recupera un enumerador de los marcas de representación para el intervalo especificado.
ms.assetid: fe060eab-8a6b-4eb7-9c7f-353b887657d8
keywords:
- Método GetRenderingMarkup marco de trabajo de servicios de texto
- Método GetRenderingMarkup marco de trabajo de servicios de texto, interfaz ITfContextRenderingMarkup
- ITfContextRenderingMarkup interface Text Services Framework, método GetRenderingMarkup
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup.GetRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f3ccfb97af6a6657c33982359640a2a924cad2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792567"
---
# <a name="itfcontextrenderingmarkupgetrenderingmarkup-method"></a><span data-ttu-id="1f50d-106">ITfContextRenderingMarkup:: GetRenderingMarkup (método)</span><span class="sxs-lookup"><span data-stu-id="1f50d-106">ITfContextRenderingMarkup::GetRenderingMarkup method</span></span>

<span data-ttu-id="1f50d-107">El método **ITfContextRenderingMarkup:: GetRenderingMarkup** recupera un enumerador de los marcas de representación para el intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="1f50d-107">The **ITfContextRenderingMarkup::GetRenderingMarkup** method retrieves an enumerator of the rendering markups for the given range.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f50d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f50d-108">Syntax</span></span>


```C++
HRESULT GetRenderingMarkup(
  [in]  TfEditCookie           ec,
  [in]  DWORD                  dwFlags,
  [in]  ITfRange               *pRangeCover,
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="1f50d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f50d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f50d-110">*EC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1f50d-110">*ec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f50d-111">\[en \] una cookie de edición de solo lectura para tener acceso al contexto.</span><span class="sxs-lookup"><span data-stu-id="1f50d-111">\[in\] A read only edit cookie to access the context.</span></span>

</dd> <dt>

<span data-ttu-id="1f50d-112">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1f50d-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f50d-113">\[in\]</span><span class="sxs-lookup"><span data-stu-id="1f50d-113">\[in\]</span></span>



| <span data-ttu-id="1f50d-114">Value</span><span class="sxs-lookup"><span data-stu-id="1f50d-114">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="1f50d-115">Significado</span><span class="sxs-lookup"><span data-stu-id="1f50d-115">Meaning</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="TF_GRM_INCLUDE_PROPERTY"></span><span id="tf_grm_include_property"></span><dl> <span data-ttu-id="1f50d-116"><dt>**\_propiedad de \_ inclusión TF GRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f50d-116"><dt>**TF\_GRM\_INCLUDE\_PROPERTY**</dt></span></span> </dl> | <span data-ttu-id="1f50d-117">Si este bit es 1, el enumerador incluirá la \_ propiedad del atributo prop de GUID \_ .</span><span class="sxs-lookup"><span data-stu-id="1f50d-117">If this bit is 1, the enumerator will include the GUID\_PROP\_ATTRIBUTE property.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1f50d-118">*pRangeCover* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1f50d-118">*pRangeCover* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f50d-119">\[en \] un puntero a una interfaz [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) del intervalo para enumerar los marcas de representación.</span><span class="sxs-lookup"><span data-stu-id="1f50d-119">\[in\] A pointer to an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) interface of the range to enumerate the rendering markups.</span></span>

</dd> <dt>

<span data-ttu-id="1f50d-120">*ppEnum* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1f50d-120">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f50d-121">\[\]un puntero para recuperar el puntero de la interfaz [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) .</span><span class="sxs-lookup"><span data-stu-id="1f50d-121">\[out\] A pointer to retrieve [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f50d-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f50d-122">Return value</span></span>

<span data-ttu-id="1f50d-123">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="1f50d-123">This method can return one of these values.</span></span>



| <span data-ttu-id="1f50d-124">Value</span><span class="sxs-lookup"><span data-stu-id="1f50d-124">Value</span></span>                                                                                | <span data-ttu-id="1f50d-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f50d-125">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="1f50d-126"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1f50d-126"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1f50d-127">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1f50d-127">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1f50d-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f50d-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1f50d-129">Este método no está actualmente en los archivos de encabezado públicos.</span><span class="sxs-lookup"><span data-stu-id="1f50d-129">This method is not currently in the public header files.</span></span> <span data-ttu-id="1f50d-130">Para usar esta API, debe compilar MIDL en el [prototipo](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="1f50d-130">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

