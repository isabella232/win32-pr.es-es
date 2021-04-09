---
description: Recupera el nombre del proveedor de IInkAnalysisRecognizer.
ms.assetid: 62ff209e-2a34-4c04-90a0-661d06898298
title: 'IInkAnalysisRecognizer:: GetVendor (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetVendor
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a48bec62ed4a6a9d94d54ea3a1ba4a53eddd4b7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154424"
---
# <a name="iinkanalysisrecognizergetvendor-method"></a><span data-ttu-id="ee901-103">IInkAnalysisRecognizer:: GetVendor (método)</span><span class="sxs-lookup"><span data-stu-id="ee901-103">IInkAnalysisRecognizer::GetVendor method</span></span>

<span data-ttu-id="ee901-104">Recupera el nombre del proveedor de [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="ee901-104">Retrieves the vendor name of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ee901-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee901-105">Syntax</span></span>


```C++
HRESULT GetVendor(
  [out] BSTR *pbstrVendor
);
```



## <a name="parameters"></a><span data-ttu-id="ee901-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee901-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee901-107">*pbstrVendor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ee901-107">*pbstrVendor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee901-108">Nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="ee901-108">The name of the vendor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee901-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee901-109">Return value</span></span>

<span data-ttu-id="ee901-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ee901-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ee901-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee901-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ee901-112">Para evitar una pérdida de memoria, llame a [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) en \* *pbstrVendor* cuando ya no necesite usar la cadena.</span><span class="sxs-lookup"><span data-stu-id="ee901-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrVendor* when you no longer need to use the string.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ee901-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee901-113">Requirements</span></span>



| <span data-ttu-id="ee901-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee901-114">Requirement</span></span> | <span data-ttu-id="ee901-115">Value</span><span class="sxs-lookup"><span data-stu-id="ee901-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee901-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee901-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ee901-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ee901-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ee901-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee901-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ee901-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ee901-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ee901-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee901-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee901-121"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ee901-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ee901-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ee901-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee901-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee901-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ee901-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee901-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee901-125">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="ee901-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="ee901-126">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="ee901-126">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

