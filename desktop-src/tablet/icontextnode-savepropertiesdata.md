---
description: Recupera una matriz de bytes que contiene los datos de propiedad internos y específicos de la aplicación para este IContextNode.
ms.assetid: f26d71a7-fe71-48a8-9c8f-9c4d99261df1
title: 'IContextNode:: SavePropertiesData (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SavePropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f2ac064632eb9e5dd2b94f6e75b9b2836c75996d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001188"
---
# <a name="icontextnodesavepropertiesdata-method"></a><span data-ttu-id="948f2-103">IContextNode:: SavePropertiesData (método)</span><span class="sxs-lookup"><span data-stu-id="948f2-103">IContextNode::SavePropertiesData method</span></span>

<span data-ttu-id="948f2-104">Recupera una matriz de bytes que contiene los datos de propiedad internos y específicos de la aplicación para este [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="948f2-104">Retrieves an array of bytes that contains the application-specific and internal property data for this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="948f2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="948f2-105">Syntax</span></span>


```C++
HRESULT SavePropertiesData(
  [in, out] ULONG *pulPropertiesDataSize,
  [out]     BYTE  **ppbPropertiesData
);
```



## <a name="parameters"></a><span data-ttu-id="948f2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="948f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="948f2-107">*pulPropertiesDataSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="948f2-107">*pulPropertiesDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="948f2-108">Tamaño de la matriz de datos que contiene la información de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="948f2-108">The size of the data array containing the property information.</span></span> <span data-ttu-id="948f2-109">No se utiliza el valor pasado en.</span><span class="sxs-lookup"><span data-stu-id="948f2-109">The value passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="948f2-110">*ppbPropertiesData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="948f2-110">*ppbPropertiesData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="948f2-111">Puntero a una matriz de enteros de 8 bits sin signo que contiene los datos de propiedad internos y específicos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="948f2-111">A pointer to an 8-bit unsigned integer array that contains the application-specific and internal property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="948f2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="948f2-112">Return value</span></span>

<span data-ttu-id="948f2-113">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="948f2-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="948f2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="948f2-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="948f2-115">Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppbPropertiesData* cuando ya no necesite la información.</span><span class="sxs-lookup"><span data-stu-id="948f2-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbPropertiesData* when you no longer need the information.</span></span>

 

<span data-ttu-id="948f2-116">Use este método cuando la aplicación mantenga su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="948f2-116">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="948f2-117">Este método guarda los datos de propiedad que **IInkAnalyzer** ha establecido en [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="948f2-117">This method saves the property data that the **IInkAnalyzer** has set on the [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="948f2-118">Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="948f2-118">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="948f2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="948f2-119">Requirements</span></span>



| <span data-ttu-id="948f2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="948f2-120">Requirement</span></span> | <span data-ttu-id="948f2-121">Value</span><span class="sxs-lookup"><span data-stu-id="948f2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="948f2-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="948f2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="948f2-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="948f2-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="948f2-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="948f2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="948f2-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="948f2-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="948f2-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="948f2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="948f2-127"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="948f2-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="948f2-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="948f2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="948f2-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="948f2-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="948f2-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="948f2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="948f2-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="948f2-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="948f2-132">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="948f2-132">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="948f2-133">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="948f2-133">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="948f2-134">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="948f2-134">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="948f2-135">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="948f2-135">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="948f2-136">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="948f2-136">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="948f2-137">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="948f2-137">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="948f2-138">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="948f2-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

